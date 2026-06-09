// ============================================================================
// Nerdio Microlearning Carousel renderer
// ============================================================================
// Renders a multi-page A4 portrait HTML carousel to vector PDF for LinkedIn.
//
// Usage:
//   node microlearning_render_carousel.js input.html output.pdf
//
// The HTML must use:
//   - @page { size: A4 portrait; margin: 0 } in CSS
//   - One <section class="slide"> per page
//   - page-break-after: always on .slide (last slide may opt out)
//
// Output is a true VECTOR PDF (selectable text, infinitely sharp on LinkedIn).
// ============================================================================
 
const puppeteer = require('puppeteer-core');
const path = require('path');
 
(async () => {
  if (process.argv.length < 4) {
    console.error('Usage: node microlearning_render_carousel.js <input.html> <output.pdf>');
    process.exit(1);
  }
 
  const inputPath = path.resolve(process.argv[2]);
  const outputPath = path.resolve(process.argv[3]);
 
  const browser = await puppeteer.launch({
    executablePath: '/home/claude/.cache/puppeteer/chrome/linux-131.0.6778.204/chrome-linux64/chrome',
    args: ['--no-sandbox', '--disable-setuid-sandbox', '--disable-dev-shm-usage'],
    headless: 'new',
  });
  const page = await browser.newPage();
 
  // A4 portrait at 96 dpi: 794 x 1123 px. deviceScaleFactor 2 for crisp output.
  await page.setViewport({ width: 794, height: 1123, deviceScaleFactor: 2 });
 
  await page.goto('file://' + inputPath, { waitUntil: 'networkidle0' });
 
  // Wait for Google Fonts to load (Poppins, Fraunces, IBM Plex Mono).
  // Without this delay, the PDF may render with fallback fonts.
  await new Promise(r => setTimeout(r, 3000));
 
  await page.pdf({
    path: outputPath,
    format: 'A4',
    landscape: false,
    printBackground: true,
    margin: { top: '0mm', right: '0mm', bottom: '0mm', left: '0mm' },
    preferCSSPageSize: true,
  });
 
  await browser.close();
  console.log('Vector PDF written:', outputPath);
})().catch(e => {
  console.error('Render failed:', e);
  process.exit(1);
});