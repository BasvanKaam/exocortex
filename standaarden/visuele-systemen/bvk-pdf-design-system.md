Allowed flexibilityHard rulesVary step count if content warrantsUse exact color palette belowReuse blocks (TODAY/WITH, stats grid, chips, q-cards) on any pageUse exact type scale belowAdd an architecture-diagram page using BvK skin tokensStripe bands on every page (top always, bottom on dark only)Adjust body text length to fit page distributionCover always dark, content always cream, insight always darkAdd a new component pattern if existing ones don't fitPop word reserved for cover/quote/takeaway onlySwap pop word per lesson (Agents, Hybrid, Compass, etc.)bvk. wordmark on cover, footer is BvK Microlearning · TOPICUse a stats grid on a different page if the data calls for itFooter page number always outlined retro Bowlby

When in doubt: match the visual weight, distribution, and rhythm of the rendered W365 for Agents lesson.



2\. Brand framing

BvK is editorial, opinionated, anti-corporate. Tagline: "Short reads. Sharp takes. No fluff." Reader is an engineer wanting signal not slides. The PDF is an artifact with 70s magazine spine and weight.

Voice rules (applied to body and inline writing):



Sentence case in body; tracked caps stay ALL CAPS as stylistic treatment

No em dashes — use comma, colon, parentheses

"Built / by night" cheekiness over corporate polish

One pop word per hero, never more

Steps "earn their time" — every fact has to add insight, no filler

When tightening text on dense pages (especially p5), drop words like "currently", "explicitly", "Microsoft" (where context provides it), "The agent" (where implied), "Compute is" (where redundant)





3\. Color palette

3.1 Brand colors

css:root {

&#x20; --coffee:      #2a1810;  /\* dark page bg, body text on cream \*/

&#x20; --rust:        #6a2410;  /\* tertiary text, hairlines, footer caps on cream, step 0 circle \*/

&#x20; --brick:       #C21717;  /\* cover shadow, item 3 stroke, step 4 circle, deepest accent \*/

&#x20; --orange:      #E76219;  /\* primary accent, pop in dek, dots, step 3 circle, item 1 stroke \*/

&#x20; --mustard:     #FEA712;  /\* primary pop word on dark, tracked caps on dark, item 4 stroke \*/

&#x20; --teal:        #4a9b95;  /\* cool tegenwicht, cluster color, dek emphasis, step 1 circle, item 2 stroke \*/

&#x20; --mint:        #7BC2BC;  /\* cover dek color, item 5 dot, secondary cool \*/

&#x20; --cream:       #fcf6e8;  /\* page background — content pages \*/

&#x20; --cream-warm:  #f5e3c1;  /\* accent block backgrounds: Today, question cards \*/

}

3.2 Surface tints

UseValueSubtle card panel bg (p4)rgba(245,227,193,0.55)Footer bg on cream pagesrgba(106,36,16,0.05)Footer bg on dark pagesrgba(245,227,193,0.05)Footer top border on creamrgba(106,36,16,0.16)Footer top border on darkrgba(245,227,193,0.16)Hairline horizontal rule on creamrgba(106,36,16,0.22)Block border on accent blocksaccent color at 30-40% opacityDashed rule on stats gridrgba(106,36,16,0.4)With-block bgrgba(74,155,149,0.13)With-block borderrgba(74,155,149,0.35)Code span bgrgba(106,36,16,0.08)Pill bgrgba(106,36,16,0.10)Cover-foot borderrgba(245,227,193,0.30)

3.3 Color usage rules



Mustard #FEA712: pop word on dark backgrounds, tracked caps labels on dark, item 4 in cycle

Orange #E76219: primary brand accent, dots, dek inline emphasis, item 3 circle

Brick #C21717: cover shadow only, item 3 stroke (p2), step 4 circle (p5)

Teal #4a9b95: cluster color (left half of p4 cards), step 1 circle, inline italic phrase emphasis in H1

Rust #6a2410: text on cream-page footer, secondary text, step 0 circle, hairlines

Mint #7BC2BC: cover italic dek only, item 5 dot in spec list





4\. Typography

4.1 Fonts and sources

UseFontWeightSourceCover hero (rendered as SVG)Bowlby One400@fontsource/bowlby-oneContent H1Yeseva One400@fontsource/yeseva-oneOutlined retro numerals (p2)Bowlby One via SVG400@fontsource/bowlby-oneWordmark bvk.Bowlby One400@fontsource/bowlby-oneStats numerals (p7, .stat-num + .headline-num)Fraunces700@fontsource/frauncesStep circles (p5)Bowlby One400@fontsource/bowlby-oneFooter page numberBowlby One400@fontsource/bowlby-oneInsight quote marks (p6)Bowlby One400@fontsource/bowlby-oneItalic dek, intro paragraph, quote textGeorgia (system)normal italic + 700 italic for inline emphasisnativeBody text, item titles, labelssystem sans (ui-sans-serif)400, 600nativeCode spanssystem monospace (ui-monospace)400native

Both Bowlby One and Yeseva One ship single weight (400). No alternative weights.

Why Fraunces for stats (p7, May 2026 update) — Stats and the bottom callout on the in-practice slide previously used Bowlby One. Bowlby's chunky retro silhouette works for the cover hero, page numerals, step circles, and the giant insight quote marks (everywhere the type is the decoration), but it overweights the in-practice stats table, where the eye should land on the number and the comparison, not on the typeface. Fraunces 700 keeps the editorial / soft-serif BvK feel and reads as one family with Yeseva (the H1 face), while giving stats and callouts a quieter, more grown-up authority that mirrors the calm display serif Nerdio Compass uses on its in-practice page.

4.2 Type scale at A4 — final calibrated values

These are the actual rendered sizes that work. Use them directly.

COVER (page 1)

&#x20; Hero title (SVG)         font-size="220" in viewBox 1500x500 → \~62pt rendered

&#x20; Cover dek                25pt italic Georgia mint, line-height 1.32

&#x20; bvk. wordmark            17.1pt Bowlby

&#x20; Edition pill             10.8pt tracked 2.5pt

&#x20; Microlearning label      10.8pt tracked 2.5pt mustard

&#x20; "By Bas van Kaam"        17.1pt cream (name 700 weight)

&#x20; "Principal Learner Arch" 10.8pt tracked 2.2pt mustard caps

&#x20; Page number 01/08        17.1pt Bowlby cream 85%



CONTENT PAGES (2, 3, 4, 5, 7, 8)

&#x20; Step label (tracked)     10.8pt tracked 2.5pt teal (or mustard on dark)

&#x20; Content H1 (.h1c)        40pt Yeseva (smaller variant 35pt for p4/p5 longer titles)

&#x20; Italic intro/dek         17.1pt Georgia italic rust, line-height 1.5

&#x20; Body text (.bd)          14pt line-height 1.55, color coffee 84% opacity

&#x20; Item title (.it)         17.1pt weight 600 coffee, line-height 1.22

&#x20; Card mini-title (.mini-it)  14.7pt weight 600 (p4)

&#x20; Card mini-body (.mini-bd)   12.1pt opacity 0.84 (p4)

&#x20; Outlined retro numerals (SVG)  font-size="62" in viewBox 100x70 → 22mm×15.4mm rendered

&#x20; Step circle number       26.4pt Bowlby cream-color on filled colored circle (11mm × 11mm)

&#x20; Stat numeral (p7)        26pt Fraunces 700 orange, letter-spacing -0.5pt

&#x20; Headline numeral (p7)    26pt Fraunces 700 teal, letter-spacing -0.5pt

&#x20; Chip check ✓             13pt teal

&#x20; Chip title               12.4pt weight 600

&#x20; Chip body                10.8pt opacity 0.84

&#x20; Stat label               10.8pt tracked 2pt rust caps

&#x20; Q-label tracked          10.8pt tracked 2.2pt cluster-color caps

&#x20; Q-question               15.5pt weight 600

&#x20; Q-hint                   13.2pt italic Georgia rust

&#x20; Takeaway label           10.8pt tracked 2.2pt mustard caps

&#x20; Takeaway text            17.1pt cream-warm, line-height 1.45

&#x20; Share line               14pt italic Georgia rust

&#x20; Author signature         10.8pt tracked 2.2pt rust caps

&#x20; One-off pill             9.3pt tracked 1.6pt rust on rust-10% bg

&#x20; Code span                12.4pt monospace rust on rust-8% bg



INSIGHT PAGE (6)

&#x20; Step label               10.8pt tracked 2.5pt mustard caps

&#x20; Quote marks (Bowlby)     75pt orange 90% opacity, line-height 0.6

&#x20; Quote text               28pt italic Georgia cream, line-height 1.34

&#x20;   (with one mustard italic pop word/phrase inside)



FOOTER (every page)

&#x20; Tracked caps             10.1pt tracked 1.9pt with white-space: nowrap

&#x20; Page number              15.5pt Bowlby

4.3 Letter-spacing conventions

ElementLetter-spacingTracked caps labels1.9–2.5pt (varies by size, \~10–13% of font-size)Yeseva H1-0.4 to -0.6pt (tight)Bowlby hero-2.8pt (very tight, in SVG units this is letter-spacing="-7")Fraunces stats / headline (p7)-0.5ptBowlby page numbernormalWordmark bvk.-0.5ptBody text0pt

4.4 Weight conventions

UseWeightBold inline emphasis in body600 (never 700 — too heavy)Item titles, mini-titles, chip titles600Tracked caps labels600Q-question600"By Bas van Kaam" name700 (only here)Italic emphasis in H1 (teal phrase)700 italicItalic Hint: prefix in q-card700 italicAll Bowlby (cover, numerals, stats, footer page num)400 nativeAll Yeseva (content H1)400 nativeItalic dek, quote text, share line400 italicBody regular400



5\. Page format

5.1 Page container

css@page { size: A4 portrait; margin: 0; }



.page {

&#x20; width: 210mm;

&#x20; height: 297mm;

&#x20; position: relative;

&#x20; overflow: hidden;

&#x20; page-break-after: always;

&#x20; display: flex;

&#x20; flex-direction: column;

}

.page:last-child { page-break-after: auto; }

.page.dark { background: var(--coffee); color: var(--cream-warm); }

.page.cream { background: var(--cream); color: var(--coffee); }

5.2 Body content area

css.body {

&#x20; flex: 1;

&#x20; padding: 13mm 14mm 8mm;        /\* default; tighter pages override \*/

&#x20; display: flex;

&#x20; flex-direction: column;

&#x20; position: relative;

&#x20; z-index: 2;

&#x20; min-height: 0;

}

Per-page padding override:



P7 In practice: padding: 12mm 12mm 7mm (tighter horizontal to fit dense content)

P8 Now you try: padding: 12mm 12mm 7mm (same)



5.3 Stripe band heights

StripeHeightCream-page top mini stripe (4 colors)3.3mmDark-page top full stripe (5 colors)4mmDark-page bottom reversed stripe (5 colors)2.7mm

Cream pages have no bottom stripe — the footer bar terminates the page.



6\. Universal elements (every page)

6.1 Top stripe band

Cream pages: 4-color stripe, left→right: teal #4a9b95, mustard #FEA712, orange #E76219, brick #C21717.

Dark pages: 5-color stripe, left→right: teal, mustard, orange, brick, rust #6a2410.

html<div class="stripe st-top-cream">

&#x20; <div style="background:#4a9b95"></div>

&#x20; <div style="background:#FEA712"></div>

&#x20; <div style="background:#E76219"></div>

&#x20; <div style="background:#C21717"></div>

</div>

For dark pages add the fifth rust segment.

6.2 Bottom stripe band (dark pages only)

Order reversed: rust, brick, orange, mustard, teal. Height 2.7mm.

6.3 Vertical rainbow stripes (dark pages only)

css.vstripes {

&#x20; position: absolute;

&#x20; inset: 0;

&#x20; display: flex;

&#x20; justify-content: space-evenly;

&#x20; opacity: 0.04;     /\* 4% at A4 print \*/

&#x20; pointer-events: none;

&#x20; z-index: 1;

}

.vstripes > div { width: 3mm; }

Five vertical stripes in order: teal, mint, mustard, orange, brick. Each 3mm wide.

6.4 Radial glows (dark pages only)

css.glow1 { background: radial-gradient(ellipse 70% 45% at 92% 22%, rgba(231,98,25,0.42), transparent 65%); }

.glow2 { background: radial-gradient(ellipse 45% 35% at 4% 75%, rgba(254,167,18,0.22), transparent 65%); }

.glow-c { background: radial-gradient(ellipse 80% 60% at 50% 50%, rgba(231,98,25,0.32), transparent 65%); }

Cover (p1): .glow1 + .glow2.

Insight (p6): .glow-c + .glow2 (center glow instead of top-right).

All glow elements absolutely positioned with inset: 0 and z-index: 1.

6.5 Footer bar

css.footer {

&#x20; display: flex;

&#x20; justify-content: space-between;

&#x20; align-items: center;

&#x20; padding: 2.5mm 13mm;

&#x20; background: rgba(106,36,16,0.05);   /\* cream-page variant \*/

&#x20; border-top: 0.6pt solid rgba(106,36,16,0.16);

&#x20; flex-shrink: 0;

}

.footer.dark-foot {

&#x20; background: rgba(245,227,193,0.05);

&#x20; border-top: 0.6pt solid rgba(245,227,193,0.16);

}

.ftm {

&#x20; font-size: 10.1pt;

&#x20; letter-spacing: 1.9pt;

&#x20; text-transform: uppercase;

&#x20; font-weight: 600;

&#x20; color: var(--rust);                 /\* mustard on dark \*/

&#x20; display: flex;

&#x20; align-items: center;

&#x20; gap: 1.8mm;

&#x20; white-space: nowrap;                /\* CRITICAL — prevents wrapping \*/

}

.ftn { font-family: 'Bowlby One', sans-serif; font-size: 15.5pt; color: var(--rust); }

Footer contents (always):



Burnt orange dot (1.5mm × 1.5mm circle, var(--orange))

Tracked caps: BvK Microlearning · TOPIC NAME

Outlined retro page number: XX / 08 in Bowlby



html<div class="footer">

&#x20; <div class="ftm"><span class="dot"></span>BvK Microlearning · TOPIC NAME</div>

&#x20; <div class="ftn">02 / 08</div>

</div>

6.6 Wordmark

bvk. set in Bowlby One. The period in burnt orange. The "bvk" body in contextual color (cream on dark, coffee on cream).

Appears on cover (top-left, \~17.1pt). Not repeated on content pages — the footer's BvK Microlearning text serves as the brand identifier.



7\. Page-by-page specifications

7.1 Page 1 — Cover (dark)

Background: deep coffee. Top stripe 5-color (4mm). Bottom stripe 5-color reversed (2.7mm). Both radial glows. Vertical rainbow stripes.

Layout (top to bottom inside .body):



Top row: bvk. wordmark left | "Edition 2026" pill right



Pill: 10.8pt tracked 2.5pt mustard text, 0.4pt mustard border at 50% opacity, padding 1.4mm × 3.2mm, border-radius 99pt





Spacer: \~28mm margin-top before Microlearning row

Microlearning row: 5mm × 0.4mm mustard line + "Microlearning" label tracked 2.5pt mustard

Hero title (SVG, 5mm margin-top):



viewBox 1500x500, rendered at 150mm × 50mm, overflow: visible

Brick-red shadow layer first: <text x="40" y="200" font-family="Bowlby One" font-size="220" letter-spacing="-7" fill="#C21717">Windows 365</text> and second line at y="420"

Cream front layer next: same coordinates but x="0", y="180" and y="400"

Inside the second cream line, use <tspan fill="#f5e3c1">for </tspan><tspan fill="#FEA712">Agents</tspan> for the mustard pop word





Cover dek (5mm margin-top): italic Georgia 25pt mint, max-width 85%, line-height 1.32

Flex spacer: <div style="flex:1"></div> to push the foot to the bottom

Cover foot: 0.4pt cream-30% top border, 3mm padding-top, flex space-between:



Left: "By Bas van Kaam" (17.1pt, name 700) + "Principal Learner Architect" tracked caps 10.8pt mustard below

Right: page number 01 / 08 in Bowlby 17.1pt cream 85%







7.2 Page 2 — Step 1: Why this lesson (cream)

Background: cream. Top mini stripe (3.3mm). No bottom stripe.

Layout in .body:



Step label tracked 2.5pt teal: Step 1 · Why this lesson

H1 (Yeseva 40pt, margin-top 5mm): Short framing question.



May contain ONE inline italic teal phrase using <span class="sf" style="color: var(--teal); font-weight: 700;">phrase</span>

Single color overall, no mustard pop word





Container with flex:1 and justify-content: space-around to distribute the 3 items

Three step rows, separated by <div class="hr-rust"></div> (0.6pt rust hairline, 4mm vertical margin):



html<div class="step-row">

&#x20; <svg class="outline-num" viewBox="0 0 100 70" preserveAspectRatio="xMinYMid meet" width="22mm" height="15.4mm">

&#x20;   <text x="0" y="60" font-family="Bowlby One" font-size="62" fill="none" stroke="#E76219" stroke-width="2.8">01</text>

&#x20; </svg>

&#x20; <div class="step-content">

&#x20;   <div class="it">Item title (17.1pt weight 600)</div>

&#x20;   <div class="bd">Body paragraph (14pt, 1.55 line-height, coffee at 84% opacity).</div>

&#x20; </div>

</div>

Outlined numeral stroke colors (cycle):



Item 01: orange #E76219

Item 02: teal #4a9b95

Item 03: brick #C21717



.step-row styling:

css.step-row { display: flex; gap: 4mm; align-items: flex-start; }

.outline-num { font-family: 'Bowlby One', sans-serif; min-width: 12mm; line-height: 1; }

.step-content { padding-top: 0.5mm; flex: 1; }

7.3 Page 3 — Step 2: What it is (cream)

Background: cream. Top mini stripe.

Layout:



Step label tracked teal: Step 2 · What it is

H1 Yeseva 40pt: Declarative statement

Italic Georgia intro paragraph (margin-top 5mm), around 16pt at 88% opacity, line-height 1.55



Contains 2-3 inline bold italic emphases on key terms (weight 600 italic)

Use <span style="font-weight: 600; font-style: italic;">key term</span> syntax





HR-rust: 0.6pt rust hairline at 22%

Section label TOPIC AT A GLANCE rust tracked caps

Container with flex:1 and justify-content: space-around for 5 spec rows

Five spec rows:



html<div class="spec-row">

&#x20; <div class="spec-label-col">

&#x20;   <span class="dot" style="background: var(--teal)"></span>

&#x20;   <span class="it" style="font-size: 15.5pt;">Status</span>

&#x20; </div>

&#x20; <div class="bd" style="font-size: 14pt; margin-top: 0.3mm;">Body text...</div>

</div>

.spec-label-col CSS — IMPORTANT:

css.spec-label-col {

&#x20; min-width: 40mm;           /\* CRITICAL — accommodates "Prerequisites" at 17pt \*/

&#x20; display: flex;

&#x20; align-items: center;

&#x20; gap: 1.8mm;

&#x20; padding-top: 0.7mm;

}

Dot color cycle for 5 spec rows:



Teal — typically Status

Orange — typically Pricing

Brick — typically Prerequisites

Mustard — typically Architecture

Mint — typically Limits



7.4 Page 4 — Step 3: Two layers / pillars (cream)

Background: cream. Top mini stripe.

Layout:



Step label tracked teal: Step 3 · Two layers, one workforce

H1 Yeseva (35pt, slightly smaller for 2-line fit): typically two-sentence framing

Italic Georgia dek line (margin-top 2.5mm), with one inline burnt-orange emphasis phrase:

<span style="color: var(--orange)">on the roadmap</span>

2×2 grid (margin-top 4mm):



css.layers-grid {

&#x20; flex: 1;

&#x20; display: grid;

&#x20; grid-template-columns: 1fr 1fr;

&#x20; grid-template-rows: 1fr 1fr;

&#x20; gap: 3mm;

&#x20; margin-top: 4mm;

}

.layers-card {

&#x20; background: rgba(245,227,193,0.55);

&#x20; padding: 5mm 6mm 9mm;       /\* CRITICAL — 9mm bottom pads items up \*/

&#x20; border-radius: 0 0 1mm 1mm; /\* only bottom corners rounded \*/

&#x20; position: relative;

&#x20; display: flex;

&#x20; flex-direction: column;

&#x20; justify-content: space-between;

}

.layers-card.teal-top { border-top: 0.8mm solid var(--teal); }

.layers-card.orange-top { border-top: 0.8mm solid var(--orange); }

.mini-it { font-size: 14.7pt; font-weight: 600; letter-spacing: -0.1pt; line-height: 1.18; }

.mini-bd { font-size: 12.1pt; line-height: 1.42; opacity: 0.84; margin-top: 0.8mm; }

Cluster pattern:



Cards 1+2 (first group, e.g. Microsoft-side): teal-top + teal section label

Cards 3+4 (second group, e.g. Nerdio-side): orange-top + orange section label



Card content:

html<div class="layers-card teal-top">

&#x20; <div class="lbl lt" style="font-size: 9.8pt;">● Microsoft · Identity</div>

&#x20; <div class="mini-item">

&#x20;   <div class="mini-it">Mini title</div>

&#x20;   <div class="mini-bd">Mini body.</div>

&#x20; </div>

&#x20; <div class="mini-item">...</div>

&#x20; <div class="mini-item">...</div>

</div>

With justify-content: space-between on the card and the 3 mini-items + label, the items distribute vertically:



Label at top of card

Mini-item 1 below label

Mini-item 2 in middle area

Mini-item 3 at bottom



The cards in the grid are equal-height (1fr 1fr rows), so items align horizontally across cards.

The extra 4mm bottom padding (5mm 6mm 9mm) pushes the bottom item up slightly so the bottom of each card has visible breathing room.

7.5 Page 5 — Step 4: How it works (cream)

Background: cream. Top mini stripe.

Layout:



Step label tracked teal: Step 4 · How it works

H1 Yeseva 35pt — typically a quoted before-and-after framing ("From X to Y in five moves")

Step flow container with the critical settings:



css.flow-container {

&#x20; flex: 1;

&#x20; display: flex;

&#x20; flex-direction: column;

&#x20; justify-content: space-around;

&#x20; padding-top: 6mm;             /\* CRITICAL — balances visual gap above step 0 with gap below step 4 \*/

}

The padding-top: 6mm is essential: it pushes the entire step cluster down so the visual gap between the H1 last line and step 0's circle matches the gap between step 4's body text and the footer.



Five step rows: 0 through 4, with dotted vertical lines between



css.flow-row { display: flex; gap: 4mm; align-items: flex-start; }

.circ {

&#x20; width: 11mm;

&#x20; height: 11mm;

&#x20; border-radius: 50%;

&#x20; display: flex;

&#x20; align-items: center;

&#x20; justify-content: center;

&#x20; flex-shrink: 0;

&#x20; font-family: 'Bowlby One', sans-serif;

&#x20; font-size: 26.4pt;

&#x20; color: var(--cream);

&#x20; line-height: 1;

}

.dline {

&#x20; width: 0;

&#x20; border-left: 0.45mm dotted rgba(106,36,16,0.5);

&#x20; height: 6.5mm;

&#x20; margin-left: 5.4mm;

}

Circle colors (filled — including step 0):



Step 0: rust #6a2410 (prerequisite, distinct from active count)

Step 1: teal #4a9b95

Step 2: mustard #FEA712

Step 3: orange #E76219

Step 4: brick #C21717



All five circles use the same .circ class and size — step 0 is NOT dotted-outlined. It's filled rust to differentiate as the "before the count starts" item, but visually consistent with the other steps.



Step 0 specials:



Title gets a "One-off" pill next to it:







html   <div><span class="it">Confirm the three prerequisites</span><span class="pill">One-off</span></div>



Pill style: font-size: 9.3pt; letter-spacing: 1.6pt; weight 600; rust on rust-10% bg; padding 0.7mm 2.2mm; border-radius: 2mm





Inline code for UI surface names:



html   <span class="code">Intune admin centre</span>

Code style: monospace, 12.4pt, rust-8% bg, rust color, padding 0.2mm 1mm, radius 0.5mm



Body text tightening rule for p5: keep step descriptions tight. Drop "Microsoft" prefix where context allows ("Intune admin centre" not "Microsoft Intune admin centre"), drop "currently", "explicitly", "The agent", "Compute is" where implied.



7.6 Page 6 — Step 5: Insight to remember (dark)

Background: deep coffee. Top stripe 5-color (4mm). Bottom stripe 5-color reversed (2.7mm). Center radial glow (.glow-c) + bottom-left mustard glow (.glow2). Vertical rainbow stripes.

Layout:



Step label tracked 2.5pt mustard: Step 5 · The insight to remember

Quote block absolutely positioned at vertical center:



css.quote-block {

&#x20; position: absolute;

&#x20; top: 50%;

&#x20; left: 17mm;

&#x20; right: 17mm;

&#x20; transform: translateY(-50%);

}



Opening Bowlby quote mark: 75pt orange at 90% opacity, line-height 0.6



html   <div class="quote-mark">\&ldquo;</div>



Italic Georgia quote text: 28pt cream, line-height 1.34, margin-top 2mm



Contains ONE mustard italic pop word/phrase:







html   <span class="sf" style="color: var(--mustard); font-style: italic;">digital workers</span>



Closing Bowlby quote mark: 75pt orange, right-aligned



html   <div class="quote-mark close">\&rdquo;</div>

Note: Bowlby's curly quotes render as block shapes (the typeface's interpretation). This reads as retro-editorial period detail. If a more traditional curly quote is wanted, render as SVG with traditional typographic punctuation.

Footer uses dark variant: .footer.dark-foot with mustard tracked caps.

7.7 Page 7 — Step 6: In practice (cream)

Background: cream. Top mini stripe. Tighter horizontal padding: padding: 12mm 12mm 7mm.

Layout:



Step label tracked teal

H1 Yeseva 40pt — short scenario title (e.g. "The 18-supplier-portals scenario")

Inner content wrapper for proportional vertical distribution:



html<div style="flex: 1; display: flex; flex-direction: column; justify-content: space-around; margin-top: 4mm;">

&#x20; <div class="today-block">...</div>

&#x20; <div class="stats-grid">...</div>

&#x20; <div class="with-block">...</div>

</div>

This wrapper is critical — it distributes the 3 content blocks evenly down the page, giving equal whitespace between TODAY → stats → WITH → bottom.



TODAY block (scenario setup, problem):



css.today-block {

&#x20; background: var(--cream-warm);

&#x20; border: 0.6pt solid rgba(231,98,25,0.32);

&#x20; border-radius: 1.2mm;

&#x20; padding: 5mm 6mm;

&#x20; margin-top: 6mm;

}

.today-body { font-size: 14pt; line-height: 1.55; color: var(--coffee); margin-top: 1.6mm; }

Header: <div class="lbl lo" style="font-size: 10.8pt; display: flex; align-items: center; gap: 1.8mm;"><span class="dot"></span>Today</div>



Stats grid (4 columns):



css.stats-grid {

&#x20; display: grid;

&#x20; grid-template-columns: repeat(4,1fr);

&#x20; padding: 5mm 0;

&#x20; border-top: 0.6pt dashed rgba(106,36,16,0.4);

&#x20; border-bottom: 0.6pt dashed rgba(106,36,16,0.4);

&#x20; margin-top: 6mm;

}

.stat-num { font-family: 'Bowlby One', sans-serif; font-size: 23pt; color: var(--orange); line-height: 1; white-space: nowrap; }

.stat-label { font-size: 10.8pt; letter-spacing: 2pt; color: var(--rust); text-transform: uppercase; font-weight: 600; margin-top: 1.4mm; }

white-space: nowrap on .stat-num is critical — prevents "90 min" from wrapping.



WITH block (resolution):



css.with-block {

&#x20; background: rgba(74,155,149,0.13);

&#x20; border: 0.6pt solid rgba(74,155,149,0.35);

&#x20; border-radius: 1.2mm;

&#x20; padding: 5mm 6mm;

&#x20; margin-top: 6mm;

}

.with-body { font-size: 14pt; line-height: 1.5; color: var(--coffee); margin-top: 1.6mm; }

Header: <div class="lbl lt" style="font-size: 10.8pt;"><span class="dot" style="background: var(--teal)"></span>With Windows 365 for Agents</div>



Chip row inside the WITH block:



css.chip-row { display: grid; grid-template-columns: 1fr 1fr 1fr; gap: 3mm; margin-top: 5mm; }

.chip {

&#x20; background: var(--cream);

&#x20; border: 0.6pt solid rgba(74,155,149,0.4);

&#x20; border-radius: 1mm;

&#x20; padding: 3.5mm 3mm;

&#x20; text-align: center;

}

.chip-check { color: var(--teal); font-size: 13pt; line-height: 1; }

.chip-title { font-size: 12.4pt; font-weight: 600; color: var(--coffee); margin-top: 1.2mm; line-height: 1.2; }

.chip-body { font-size: 10.8pt; color: var(--coffee); opacity: 0.84; margin-top: 0.8mm; line-height: 1.38; }

Each chip: ✓ + title + body (3 lines max).



Headline row below chips (also inside WITH block):



css.headline-row {

&#x20; display: flex;

&#x20; align-items: center;

&#x20; gap: 3.5mm;

&#x20; margin-top: 5mm;

&#x20; border-top: 0.6pt solid rgba(74,155,149,0.3);

&#x20; padding-top: 4mm;

}

.headline-num { font-family: 'Bowlby One', sans-serif; font-size: 23pt; color: var(--teal); line-height: 1; letter-spacing: -0.9pt; white-space: nowrap; }

.headline-body { font-size: 11.6pt; line-height: 1.45; color: var(--coffee); flex: 1; opacity: 0.84; }

Big numeric headline left (e.g. "270 min/day"), body text right with summary.

7.8 Page 8 — Step 7: Now you try + Take-away (cream)

Background: cream. Top mini stripe. Tighter padding: padding: 12mm 12mm 7mm.

Layout:



Step label tracked teal: Step 7 · Now you try

H1 Yeseva 40pt: typically "Three questions to lock the lesson in"

Question list (margin-top 6mm):



css.q-list { margin-top: 6mm; display: flex; flex-direction: column; gap: 5mm; }

.q-card {

&#x20; background: var(--cream-warm);

&#x20; border-left: 0.9mm solid var(--teal);

&#x20; border-radius: 0 1mm 1mm 0;

&#x20; padding: 3.5mm 5mm;

}

.q-card.q-mustard { border-left-color: var(--mustard); }

.q-card.q-orange { border-left-color: var(--orange); }

.q-label { font-size: 10.8pt; letter-spacing: 2.2pt; text-transform: uppercase; font-weight: 600; color: var(--teal); }

.q-label.q-mustard-text { color: var(--mustard); }

.q-label.q-orange-text { color: var(--orange); }

.q-question { font-size: 15.5pt; font-weight: 600; line-height: 1.28; color: var(--coffee); margin-top: 1.4mm; }

.q-hint { font-family: ui-serif, Georgia, serif; font-style: italic; font-size: 13.2pt; line-height: 1.42; color: var(--rust); margin-top: 1.4mm; }

.q-hint-key { font-weight: 700; font-style: italic; }

Three question cards, left-border colors cycle: teal (Q1) → mustard (Q2) → orange (Q3). Each card has Q-label + question (item-style) + italic Hint: with cluster-colored "Hint:" prefix.

html<div class="q-card">

&#x20; <div class="q-label">Q · 01</div>

&#x20; <div class="q-question">Question text...</div>

&#x20; <div class="q-hint">

&#x20;   <span class="q-hint-key" style="color: var(--teal);">Hint:</span> Hint body...

&#x20; </div>

</div>



Take-away strip (margin-top 8mm):



css.takeaway {

&#x20; background: var(--coffee);

&#x20; color: var(--cream-warm);

&#x20; padding: 5.5mm 6.5mm;

&#x20; border-radius: 1.2mm;

&#x20; margin-top: 8mm;

&#x20; text-align: center;

&#x20; position: relative;

&#x20; overflow: hidden;

}

.takeaway-glow {

&#x20; position: absolute;

&#x20; inset: 0;

&#x20; background: radial-gradient(ellipse 70% 60% at 90% 80%, rgba(254,167,18,0.25), transparent 65%);

&#x20; pointer-events: none;

}

.takeaway-lbl { font-size: 10.8pt; letter-spacing: 2.2pt; text-transform: uppercase; font-weight: 600; color: var(--mustard); position: relative; }

.takeaway-text { font-size: 17.1pt; line-height: 1.45; margin-top: 1.8mm; position: relative; }

html<div class="takeaway">

&#x20; <div class="takeaway-glow"></div>

&#x20; <div class="takeaway-lbl">Take-away</div>

&#x20; <div class="takeaway-text">

&#x20;   First framing.<br>The second framing with <span style="color: var(--mustard); font-weight: 600;">pop phrase</span> here.

&#x20; </div>

</div>

The mustard pop phrase weight 600. Glow positioned subtly bottom-right inside the dark panel.



Share line (italic Georgia 14pt rust, margin-top 6mm, text-align center):



html   <div class="share-line">Found this useful? Share it with one colleague preparing IT for the agent workforce.</div>



Author signature (tracked caps 10.8pt rust, margin-top 4mm, text-align center):



html   <div class="author-sig">Bas van Kaam · Principal Learner Architect</div>



8\. Component patterns (reusable building blocks)

These are the proven blocks. Reuse on any page where they fit the data.

8.1 Outlined retro numeral (SVG)

html<svg class="outline-num" viewBox="0 0 100 70" preserveAspectRatio="xMinYMid meet" width="22mm" height="15.4mm">

&#x20; <text x="0" y="60" font-family="Bowlby One" font-size="62" fill="none" stroke="#E76219" stroke-width="2.8">01</text>

</svg>

Used for: page 2 step numbers. Stroke colors cycle orange / teal / brick.

8.2 Filled retro circle (step indicator)

html<div class="circ" style="background: var(--teal)">1</div>

11mm × 11mm circle, Bowlby 26.4pt cream text. Colors cycle through palette. Rust for "step 0 prerequisite" pattern.

8.3 Card with top accent border (p4 pattern)

html<div class="layers-card teal-top">

&#x20; <div class="lbl lt" style="font-size: 9.8pt;">● Cluster · Section</div>

&#x20; <div class="mini-item"><div class="mini-it">Title</div><div class="mini-bd">Body.</div></div>

&#x20; <div class="mini-item">...</div>

&#x20; <div class="mini-item">...</div>

</div>

5mm 6mm 9mm padding (extra bottom), flex space-between distribution, 2px top border in accent color.

8.4 Today-style accent block (warm)

Background cream-warm, accent-30% border 0.6pt, 1.2mm radius, padding 5mm 6mm. Used for problem-state / scenario-setup blocks.

8.5 With-style accent block (cool)

Background teal-13% tint, teal-35% border, 1.2mm radius, padding 5mm 6mm. Used for solution-state / resolution blocks.

8.6 Chip (outcome card, 3-up)

Background cream, accent-40% border 0.6pt, 1mm radius, padding 3.5mm 3mm. ✓ check + title + body, 3-line height.

8.7 Question card (left-bar)

Background cream-warm, 0.9mm solid left border in cycling accent color, 0 1mm 1mm 0 radius, padding 3.5mm 5mm.

8.8 Take-away strip (dark callout)

Background coffee, cream text, 5.5mm 6.5mm padding, 1.2mm radius, subtle mustard radial glow bottom-right, centered.

8.9 One-off pill

Tracked caps 9.3pt 1.6pt tracking, rust on rust-10% bg, 0.7mm 2.2mm padding, 2mm border-radius, inline-block.

8.10 Code span

Monospace 12.4pt, rust on rust-8% bg, 0.2mm 1mm padding, 0.5mm radius. For inline UI surface names.

8.11 Edition pill (cover only)

Tracked caps 10.8pt 2.5pt tracking, mustard text, 0.4pt mustard-50% border, 1.4mm 3.2mm padding, 99pt radius (pill shape).

8.12 Stats grid

4-column grid, top/bottom 0.6pt dashed rust-40% borders, padding 5mm 0. Big Bowlby numeral 23pt orange + small tracked caps label rust below.

8.13 Headline row (big number + body)

Inside WITH block. Top border 0.6pt teal-30%, padding-top 4mm, margin-top 5mm. Big Bowlby 23pt teal left + small body text right with flex:1.



9\. Pop word and emphasis rules

9.1 Mustard pop word

Reserved for these three positions only:



Cover hero: one mustard word/phrase inside the Bowlby SVG title

Insight quote: one mustard italic phrase inside the Georgia quote text

Take-away text: one mustard weight-600 phrase inside the take-away



Never on content page H1s, body text, footers, or tracked caps.

9.2 Inline italic teal phrase (Nerdio tradition)

For subject emphasis inside a content H1. One per H1 max.

html<span class="sf" style="color: var(--teal); font-weight: 700;">phrase</span>

The .sf class gives italic Georgia. The weight 700 makes it carry over Yeseva titles.

9.3 Inline burnt-orange dek phrase (Nerdio tradition)

For forward-looking / status callouts inside an italic Georgia dek line under H1.

html<span style="color: var(--orange)">on the roadmap</span>

9.4 Inline body bold

Weight 600, no color change. For terms reader should remember: license names, key product names.

html<span style="font-weight: 600">Microsoft Entra Agent ID</span>

9.5 Inline code

Monospace span with rust-tinted bg for UI surface names.

html<span class="code">Intune admin centre</span>



10\. Numeric system

10.1 Outlined retro numerals

Bowlby One via SVG, transparent fill, 2.8 stroke-width. Used for:



Page 2 step numbers (01, 02, 03): cycle orange / teal / brick



Always SVG, never CSS -webkit-text-stroke (WeasyPrint doesn't support it).

10.2 Filled retro circles

Bowlby One inside colored circles (11mm × 11mm), cream-color text. Used for:



Page 5 step circles (0, 1, 2, 3, 4): rust / teal / mustard / orange / brick



All five circles use the same filled style — step 0 is rust to differentiate as "prerequisite, before the count" but not visually outlined.

10.3 Solid retro stats numerals

Bowlby One in solid color. Used for:



Page 7 stats grid: solid orange 23pt

Page 7 headline (270-style): solid teal 23pt

Footer page numbers: solid rust 15.5pt (cream pages) or solid cream 15.5pt at 85% opacity (dark pages)



10.4 Number sizing guidance

The 23pt size for p7 stats and headlines is intentionally restrained — bigger feels too "grof" (heavy). The Bowlby weight at 23pt is already visually strong; bigger sizes overpower the editorial balance.



11\. Implementation: HTML + CSS

11.1 File structure

/bvk\_pdf/

&#x20; ├── lesson.html               ← single-file HTML with full lesson

&#x20; ├── lesson.pdf                ← rendered output

&#x20; ├── fonts/

&#x20; │     ├── bowlby.woff2        ← from @fontsource/bowlby-one

&#x20; │     └── yeseva.woff2        ← from @fontsource/yeseva-one

&#x20; └── node\_modules/             ← npm install location

11.2 Font setup

Install via npm (allowed in network configuration):

bashnpm install @fontsource/bowlby-one @fontsource/yeseva-one

cp node\_modules/@fontsource/bowlby-one/files/bowlby-one-latin-400-normal.woff2 fonts/bowlby.woff2

cp node\_modules/@fontsource/yeseva-one/files/yeseva-one-latin-400-normal.woff2 fonts/yeseva.woff2

Load via @font-face:

css@font-face { font-family: 'Bowlby One'; src: url('fonts/bowlby.woff2') format('woff2'); font-weight: 400; font-style: normal; }

@font-face { font-family: 'Yeseva One'; src: url('fonts/yeseva.woff2') format('woff2'); font-weight: 400; font-style: normal; }

11.3 Render to PDF

pythonfrom weasyprint import HTML

HTML('lesson.html').write\_pdf('lesson.pdf')

WeasyPrint 68+ handles all the design system features (radial gradients, opacity, border-radius, mm/pt units, SVG with text and stroke, @page A4).

11.4 Verify

Convert to PNG previews to check visually:

bashpdftoppm -r 75 lesson.pdf preview -png



12\. WeasyPrint quirks and workarounds (CRITICAL)

These rendering issues were encountered and solved during build. Apply the workarounds in every BvK build.

12.1 text-shadow doesn't render on Bowlby

Problem: text-shadow: 4pt 4pt 0 var(--brick) on a Bowlby title renders as nothing — WeasyPrint silently drops the shadow.

Solution: render the cover hero as inline SVG with two <text> layers — brick shadow first (offset), cream foreground second.

html<svg viewBox="0 0 1500 500" style="margin-top: 5mm; width: 150mm; height: 50mm; overflow: visible;">

&#x20; <text x="40" y="200" font-family="Bowlby One" font-size="220" letter-spacing="-7" fill="#C21717">Windows 365</text>

&#x20; <text x="40" y="420" font-family="Bowlby One" font-size="220" letter-spacing="-7" fill="#C21717">for Agents</text>

&#x20; <text x="0" y="180" font-family="Bowlby One" font-size="220" letter-spacing="-7" fill="#f5e3c1">Windows 365</text>

&#x20; <text x="0" y="400" font-family="Bowlby One" font-size="220" letter-spacing="-7">

&#x20;   <tspan fill="#f5e3c1">for </tspan>

&#x20;   <tspan fill="#FEA712">Agents</tspan>

&#x20; </text>

</svg>

The mustard pop word goes inside a <tspan> on the cream layer.

12.2 Outlined text via webkit-text-stroke not supported

Problem: -webkit-text-stroke-color and -webkit-text-stroke-width are silently dropped.

Solution: render outlined retro numerals as SVG with fill="none" stroke="#color" stroke-width="2.8". See section 8.1.

12.3 Footer text wrapping

Problem: BvK Microlearning · TOPIC NAME in tracked caps wraps to two lines because of letter-spacing.

Solution:



Use white-space: nowrap on .ftm

Use letter-spacing 1.9pt (not higher) on .ftm



12.4 Mm units in text-shadow

Problem: text-shadow: 1.4mm 1.4mm 0 color doesn't render.

Solution: avoid mm units in text-shadow. Use px or pt. (But for cover hero we use SVG anyway per 12.1.)

12.5 Mockup-to-A4 scale calibration

Problem: design system pt values from a small mockup widget don't translate 1:1 to A4 because the rendering scale changes.

Solution: when migrating mockup values to A4, multiply pt by \~1.55. The values in section 4.2 above are already calibrated for direct A4 use — don't scale them again.

12.6 Italic Georgia inline emphasis class

Use the .sf class (italic Georgia serif) for inline emphasis phrases in content H1s and quotes. With font-weight: 700 it carries weight in display sizes; with font-weight: 400 (default italic) it stays understated in body text.



13\. Flexibility — where to deviate and where not to

13.1 Things you can flex per lesson

ElementVariabilityLesson titlePick a hook with one mustard pop word potentialPop word on coverPick one word (Agents, Hybrid, Compass, Flex, etc.)Insight quote phraseOne mustard italic phrase inside the quoteTake-away pop phraseOne mustard weight-600 phraseItalic teal H1 phraseOptional, one per H1 maxItalic orange dek phraseOptional, one per dek line maxSpec-row dot colors (p3)Cycle through palette; order can adjustCard cluster grouping (p4)Teal-side / orange-side can map to whatever clusters fit the topicNumber of steps in step flow (p5)Typically 5 but can be 3-6Stats grid columns (p7)4 columns is standard but can be 3 if data is fewerChips per row (p7)3 standard, can be 2 or 4Number of question cards (p8)3 standard, can be 2-4Page count8 standard for full lesson, can be 6-10

13.2 Things to keep fixed

ElementFixedColor paletteUse exact hex codes, no substitutesType scaleUse the calibrated A4 pt values from section 4.2Bowlby + Yeseva pairingBowlby for cover/numerals/wordmark/stats, Yeseva for content H1Italic Georgia for dek/quoteAlways Georgia italic, not Yeseva italicMustard pop word: cover/quote/takeaway onlyNever on content H1sCover always dark coffee bgBrick-red drop shadow on heroInsight always dark coffee bgCentered quote with Bowlby quote marksStripe band on every pageTop always; bottom only on dark pagesbvk. wordmark on coverTop-left, orange periodFooter format: `● BvK Microlearning · TOPICXX / 08`Outlined retro numerals on p2Always SVG, cycle orange/teal/brickStep circles on p5Always filled, cycle rust/teal/mustard/orange/brickAll page numbers in BowlbyOutlined retro style

13.3 Adding new components

If a lesson needs a new layout (e.g. an architecture diagram page from AVD Hybrid + Nutanix), build it using:



The color palette (section 3)

The type scale (section 4.2)

The block paddings and radius conventions (1.2mm radius standard, 0.6pt borders, accent-30% to 40% opacity for borders)

Cream paper background for content pages, coffee for dark moments

Top stripe band per page-type convention



Existing diagram-slide patterns from Nerdio template can be reskinned — apply BvK tokens, keep the layout structure.



14\. Build process

14.1 Pre-build checklist



Confirm template choice with Bas: BvK or Nerdio?

Identify topic: lesson title, one-line hook, pop word for cover

Identify the insight: one phrase the reader should walk away with (for p6 quote)

Identify the take-away pop phrase: one phrase for p8

Map content to 8 steps: Why / What it is / Architecture clusters / How it works / Insight / In practice / Now you try / Take-away

Verify facts: every figure, date, dollar amount, percentage, product name must be sourced



14.2 Build steps



Copy the canonical lesson.html as starting template

Update the <title> and footer "TOPIC NAME"

Swap cover hero SVG: lesson title + mustard pop word

Swap cover dek subtitle

Page 2: Why this lesson — 3 framing items

Page 3: What it is — italic intro paragraph + 5 spec rows

Page 4: Two clusters / architecture — 4 cards in 2x2 (teal-side / orange-side)

Page 5: How it works — 5 step rows (or fewer/more if needed)

Page 6: Insight — italic quote with one mustard pop phrase

Page 7: In practice — scenario (Today block) → stats grid → resolution (With block) with chips and headline

Page 8: Now you try — 3 question cards (or 2-4) → take-away strip → share line → author signature

Render via WeasyPrint

Convert pages to PNG and verify visually

Iterate on any issues

Save final PDF to /mnt/user-data/outputs/ with descriptive filename



14.3 File naming convention

Nerdio\_<TopicSlug>\_MicroLesson\_BvK.pdf

Examples:



Nerdio\_W365\_Agents\_MicroLesson\_BvK.pdf

Nerdio\_AVDHybrid\_Nutanix\_MicroLesson\_BvK.pdf

Nerdio\_Compass\_MicroLesson\_BvK.pdf





15\. Quality checklist (before delivery)



&#x20;Cover hero brick-red shadow visible (SVG approach used)

&#x20;Mustard pop word on cover hero

&#x20;All 8 footer page numbers correct (01/08 to 08/08)

&#x20;Footer "BvK Microlearning · TOPIC NAME" doesn't wrap

&#x20;Page 2 outlined retro numerals are properly sized (22mm wide, not tiny)

&#x20;Page 3 spec-label-col is 40mm minimum (no overflow)

&#x20;Page 4 mini-items distribute evenly with horizontal alignment across cards

&#x20;Page 4 cards have visible bottom whitespace (9mm padding-bottom)

&#x20;Page 5 step 0 circle is filled rust (not dotted)

&#x20;Page 5 step cluster is shifted down by \~6mm via padding-top

&#x20;Page 5 step 0 has "One-off" pill

&#x20;Page 5 inline code spans render with rust-tinted bg

&#x20;Page 6 quote is centered both horizontally and vertically

&#x20;Page 6 mustard italic pop phrase inside quote

&#x20;Page 6 has bottom stripe band (reversed 5-color)

&#x20;Page 7 content blocks (TODAY, stats, WITH) distribute evenly via flex space-around wrapper

&#x20;Page 7 big numerals are 23pt (not 28pt+)

&#x20;Page 7 stats grid has dashed top/bottom borders

&#x20;Page 7 "270-style" headline has teal top border above it

&#x20;Page 8 question cards have cycling left-border colors (teal / mustard / orange)

&#x20;Page 8 take-away has mustard radial glow bottom-right

&#x20;Page 8 share line and author signature distributed below take-away

&#x20;All cream pages have orange-dot prefix in footer

&#x20;All dark pages have mustard tracked caps in footer

&#x20;No em dashes in body text

&#x20;No invented features or unverified claims

&#x20;All facts and figures verbatim from source





16\. Reference output

The canonical rendered example for this design system is:

/mnt/user-data/outputs/Nerdio\_W365\_Agents\_MicroLesson\_BvK.pdf

When in doubt about visual weight, rhythm, or distribution, compare to this file. It's the source of truth.

The HTML source is at:

/home/claude/bvk\_pdf/lesson.html

This is the canonical build template. Future lessons should start by copying this file and swapping content while preserving structure.



17\. Number Sheet variant (landscape A4 cheat sheet)

Locked-in May 16, 2026. Born out of the W365 for Agents Number Sheet build.

17.1 Purpose and when to use

The Number Sheet is a single-page landscape A4 companion to a full BvK lesson. It is a scan-reference, not a storytelling artifact. Where the 8-step lesson teaches why something works, the Number Sheet shows what the numbers are — pricing, limits, lifecycle, architecture — so a reader can pin it next to a screen and glance at it.

Use it when:



The lesson has 3+ memorable numbers (pricing, time savings, capacity limits, free trial hours, etc.).

The audience already knows the why and just needs to look up the what.

A field engineer or buyer wants one A4 they can take into a meeting.



Don't use it when:



The lesson is conceptual without quantitative anchors.

The reader needs to learn the topic for the first time (use the 8-step lesson).

The numbers don't dominate the reader's actual decision (then a typographic layout serves better than a number-anchored one).



17.2 Design principles (these are the rules, always)

These principles transfer across any topic. They are the what makes a Number Sheet a Number Sheet. If you deviate from one of these you've made a different kind of document.



Typography does all the work; no card surfaces. Hierarchy comes from size, color, and whitespace — never from boxes, borders, drop-shadows, or filled panels. The full-lesson uses card surfaces (Today block, with block, q-cards); the Number Sheet refuses them.

One dominant typographic layer dwarfs everything else. Whether that's 4 huge stats, 1 massive quote, or 2 enormous comparisons — something on the page is at least 3× larger than the body text. Without that dominance there's no scan-anchor and the page becomes a brochure.

One pop only. A single take-away element at the top with one orange-Fraunces or mustard accent phrase. Never two pops, never a pop in body text, never a pop in the architecture detail rows.

No "Step 1 / Step 2" section labels, no chapter numbering, no Why-What-How structure. This is reference content, not narrative. The reader scans; they don't read in order.

Color is structural, not decorative. Each accent color earns its placement (mustard for the pricing pop, orange for outcomes, brick for cost/scarcity, teal for favorable / trial / cool counterweight). Pick which color belongs to which slot based on content meaning, not visual rotation.

Perfectly aligned, evenly balanced whitespace. Within any horizontal row of items, all items align on the same baselines (label-top, number-baseline, caption-bottom). Vertical gaps between sections are equal (default 4mm body-area gap). No section has materially more breathing room than another.

Single landscape page, always. If content doesn't fit on one A4 landscape, it's not a Number Sheet — it's the wrong format for the topic. Reduce scope, not page count.

BvK palette and type system, no substitutes. Cream paper, deep coffee text, the 6-accent palette from section 3.1. Fonts: Yeseva (slim header), Fraunces 700 (all numerals + tracked labels), Georgia (italic dek + quote text), Bowlby (step circles, wordmark). Same as full-lesson — no new typefaces, no new colors.



17.3 Layout grid (default recipe)

The W365 for Agents Number Sheet is the canonical implementation of the principles above. It assembles 5 components in this order: take-away banner (top) → big number wall (4 hero stats) → micro-stats strip (5–7 medium stats) → architecture stack (3 typographic layers) → vertical numbered flow (5-step lifecycle). Sections 17.4–17.7 specify each of these 5 components in detail. This is the recipe you start from for most W365 / AVD / Microsoft-platform topics — they tend to have pricing, capacity, an identity/compute/operations split, and a deployment lifecycle, so the components map cleanly. Section 17.9 (Substitutions) covers what to do when the topic doesn't map cleanly.

Page is A4 landscape (297mm × 210mm), body padding 4mm 14mm 3mm.

┌──────────────────────────────────────────────────────────────────────────┐

│ 4-color stripe band (2.4mm)                                                │

│                                                                            │

│ HEADER row (slim, \~14mm):                                                  │

│   Yeseva H1 17pt · italic dek inline · meta tracked caps · author          │

│                                                                            │

│ ─────────────── hairline ───────────────                                   │

│                                                                            │

│ TAKE-AWAY BANNER (12mm) — full width with 1pt coffee bottom border         │

│   TAKE-AWAY label (brick Fraunces 7.6pt) + Georgia italic 14pt + orange pop│

│                                                                            │

│ ════ BIG NUMBER WALL ════ 4 columns separated by 0.5pt vertical rules     │

│   ┌────────────┬────────────┬────────────┬────────────┐                  │

│   │  TAG-LABEL │  TAG-LABEL │  TAG-LABEL │  TAG-LABEL │  (rust 7pt tracked) │

│   │            │            │            │            │                   │

│   │   $0.40    │   270 m    │   $0.24    │    50 h    │  (Fraunces 78pt)  │

│   │  / unit    │  / context │  / context │  / context │  (Fraunces 14pt)  │

│   │            │            │            │            │                   │

│   │  caption   │  caption   │  caption   │  caption   │  (8.4pt body)     │

│   └────────────┴────────────┴────────────┴────────────┘                  │

│                                                                            │

│ ──── MICRO-STATS STRIP ──── 5-7 medium stats, top+bottom 0.5pt rules      │

│   N lbl │ N lbl │ N lbl │ N lbl │ N lbl │ N lbl  (Fraunces 19pt + 7pt)    │

│                                                                            │

│ LOWER ROW (grid 1.4fr / 1fr):                                              │

│   ┌────────────────────────────┐   ┌──────────────────────┐               │

│   │ Architecture in three layers│   │ The flow · five moves │               │

│   │ (section-h with rust tag)   │   │ (section-h with tag)   │               │

│   │                              │   │                        │               │

│   │ Identity   GA      detail    │   │  ① title / body       │               │

│   │ Compute    GA      detail    │   │  ② title / body       │               │

│   │ Operations Roadmap detail    │   │  ③ title / body       │               │

│   │ (28mm / 26mm / 1fr grid)     │   │  ④ title / body       │               │

│   │                              │   │  ⑤ title / body       │               │

│   └────────────────────────────┘   └──────────────────────┘               │

│                                                                            │

│ ─────────────── footer hairline ───────────────                            │

│   bvk.   ·   TOPIC · Number Sheet · V1.0   ·   italic disclaimer right    │

└──────────────────────────────────────────────────────────────────────────┘

17.4 Specific component specifications

Take-away banner

css.take-banner {

&#x20; display: flex;

&#x20; align-items: baseline;

&#x20; gap: 4mm;

&#x20; padding: 0 0 3mm;

&#x20; border-bottom: 1pt solid var(--coffee);

&#x20; margin-bottom: 4mm;

}

.take-banner .label {

&#x20; font-family: 'Fraunces', Georgia, serif;

&#x20; font-weight: 700;

&#x20; font-size: 7.6pt;

&#x20; letter-spacing: 2pt;

&#x20; text-transform: uppercase;

&#x20; color: var(--brick);

}

.take-banner .quote {

&#x20; font-family: Georgia, serif;

&#x20; font-style: italic;

&#x20; font-size: 14pt;

&#x20; line-height: 1.32;

&#x20; color: var(--coffee);

}

.take-banner .quote .pop {

&#x20; color: var(--orange);

&#x20; font-weight: 700;

&#x20; font-style: normal;

&#x20; font-family: 'Fraunces', Georgia, serif;

}

The pop phrase is Fraunces 700 in orange, not Georgia italic. It interrupts the italic flow with a typographic stab — the editorial equivalent of the mustard pop word on a full-lesson cover.

Big number wall (4 hero stats)

css.num-wall {

&#x20; display: grid;

&#x20; grid-template-columns: 1.15fr 1fr 0.85fr 0.95fr;  /\* adjusts to content widths \*/

&#x20; gap: 0;

&#x20; margin-bottom: 4mm;

}

.big-stat {

&#x20; padding: 0 6mm;

&#x20; border-right: 0.5pt solid rgba(106,36,16,0.25);

}

.big-stat:first-child { padding-left: 0; }

.big-stat:last-child { padding-right: 0; border-right: none; }

.bs-tag {

&#x20; font-family: 'Fraunces', Georgia, serif;

&#x20; font-weight: 700;

&#x20; font-size: 7pt;

&#x20; letter-spacing: 2pt;

&#x20; text-transform: uppercase;

&#x20; color: var(--rust);

&#x20; margin-bottom: 2.4mm;

}

.bs-num {

&#x20; font-family: 'Fraunces', Georgia, serif;

&#x20; font-weight: 700;

&#x20; font-size: 78pt;

&#x20; line-height: 0.86;

&#x20; letter-spacing: -3pt;

&#x20; color: var(--coffee);

}

.bs-num.mustard { color: var(--mustard); }

.bs-num.orange  { color: var(--orange); }

.bs-num.brick   { color: var(--brick); }

.bs-num.teal    { color: var(--teal); }

.bs-num .currency { font-size: 36pt; vertical-align: 18pt; letter-spacing: -1pt; margin-right: 0.5mm; }

.bs-num .sub      { font-size: 26pt; letter-spacing: -1pt; }

.bs-num .unit {

&#x20; display: block;

&#x20; font-size: 14pt;

&#x20; letter-spacing: -0.2pt;

&#x20; color: var(--coffee);   /\* always coffee, not the accent color \*/

&#x20; margin-top: 1.6mm;

&#x20; line-height: 1;

}

.bs-caption { margin-top: 3mm; font-size: 8.4pt; line-height: 1.4; color: var(--coffee); }

Critical rules:



Exactly 4 big stats. With 3 stats the wall feels sparse; with 5 the numerals get crushed below 70pt and lose impact.

Each stat gets its own accent color from {mustard, orange, brick, teal}. Pick the 4 colors that map to the content meaning (mustard for pricing-pop, orange for outcome, brick for cost, teal for trial / favorable).

Currency and sub-suffix ($, m, h) use the same color as the parent number; only the unit caption (/ VM · hour, In the 18-portal case) is coffee.

The 4 columns must visually bottom-align on the caption row. If one caption is 2 lines and another is 1, add a line break to balance — or compress the longer one. Never let them bottom-misalign.



Micro-stats strip

css.micro-strip {

&#x20; display: flex;

&#x20; justify-content: space-between;

&#x20; align-items: baseline;

&#x20; padding: 2.4mm 0;

&#x20; margin-bottom: 4mm;

&#x20; border-top: 0.5pt solid rgba(106,36,16,0.22);

&#x20; border-bottom: 0.5pt solid rgba(106,36,16,0.22);

&#x20; flex-wrap: nowrap;

}

.micro { display: flex; align-items: baseline; gap: 1.6mm; white-space: nowrap; }

.micro .num {

&#x20; font-family: 'Fraunces', Georgia, serif;

&#x20; font-weight: 700;

&#x20; font-size: 19pt;

&#x20; color: var(--coffee);

&#x20; line-height: 1;

&#x20; letter-spacing: -0.5pt;

}

.micro .num .small { font-size: 10pt; }   /\* for $ or m suffix \*/

.micro .lbl {

&#x20; font-family: 'Fraunces', Georgia, serif;

&#x20; font-weight: 700;

&#x20; font-size: 7pt;

&#x20; letter-spacing: 1.4pt;

&#x20; text-transform: uppercase;

&#x20; color: var(--rust);

}

.micro-divider {

&#x20; width: 0.4pt;

&#x20; align-self: stretch;

&#x20; background: rgba(106,36,16,0.22);

}

Critical rules:



5 to 7 micro-stats. Below 5 it looks empty; above 7 the line wraps or the labels truncate.

Labels must fit on one line each at 7pt. Allowed: Pools / env, PCs / pool, Each / day, Agent 365 / mo. Not allowed: Cloud PCs / pool (too long), Agent 365 / user / mo (3 slashes wraps).

All stats use coffee for the number, never accent colors. The big-number wall above is where the colored emphasis lives; the micro strip is neutral.



Architecture as pure typography

css.arch-line {

&#x20; display: grid;

&#x20; grid-template-columns: 28mm 26mm 1fr;

&#x20; gap: 3mm;

&#x20; padding: 2.4mm 0;

&#x20; border-bottom: 0.4pt dashed rgba(106,36,16,0.22);

&#x20; align-items: baseline;

}

.arch-line:last-child { border-bottom: none; }

.arch-layer-name {

&#x20; font-family: 'Fraunces', Georgia, serif;

&#x20; font-weight: 700;

&#x20; font-size: 11pt;

&#x20; letter-spacing: -0.2pt;

}

.arch-line.identity .arch-layer-name { color: var(--brick); }

.arch-line.compute  .arch-layer-name { color: var(--orange); }

.arch-line.ops      .arch-layer-name { color: var(--teal); }

.arch-status {

&#x20; font-family: 'Fraunces', Georgia, serif;

&#x20; font-weight: 700;

&#x20; font-size: 6.6pt;

&#x20; letter-spacing: 1.3pt;

&#x20; text-transform: uppercase;

&#x20; color: var(--rust);

}

.arch-status .by { color: var(--coffee); }   /\* the "Microsoft" / "Nerdio" half \*/

.arch-detail { font-size: 8pt; line-height: 1.4; color: var(--coffee); }

.arch-detail b { font-weight: 600; }

Critical rules:



No card backgrounds, no card borders. This is the deliberate departure from full-lesson p4 cluster cards. The Number Sheet's architecture is typographic, not boxed.

3 layers is canonical (Identity / Compute / Operations); flex to 2–4 if the topic genuinely has different layering.

Layer names use accent color (brick / orange / teal cycle); meta status uses rust + coffee split; detail body uses coffee.

Dashed bottom borders between rows. The last row has no border.



Vertical numbered flow

css.flow-vlist {

&#x20; display: flex;

&#x20; flex-direction: column;

&#x20; position: relative;

}

.flow-vlist::before {

&#x20; content: "";

&#x20; position: absolute;

&#x20; left: 5.5mm;       /\* centered on the 11mm step circle \*/

&#x20; top: 5mm;

&#x20; bottom: 5mm;

&#x20; width: 0.5pt;

&#x20; background: rgba(106,36,16,0.22);

}

.flow-step {

&#x20; display: grid;

&#x20; grid-template-columns: 11mm 1fr;

&#x20; gap: 2mm;

&#x20; align-items: baseline;

&#x20; padding: 0.8mm 0;

}

.flow-num {

&#x20; width: 11mm; height: 11mm;

&#x20; border-radius: 99pt;

&#x20; background: var(--cream);

&#x20; border: 0.6pt solid;     /\* color set per step via :nth-child \*/

&#x20; font-family: 'Bowlby One', sans-serif;

&#x20; font-size: 14pt;

&#x20; display: flex; align-items: center; justify-content: center;

&#x20; line-height: 1; letter-spacing: -1pt;

}

.flow-step:nth-child(1) .flow-num { border-color: var(--rust);    color: var(--rust); }

.flow-step:nth-child(2) .flow-num { border-color: var(--teal);    color: var(--teal); }

.flow-step:nth-child(3) .flow-num { border-color: var(--orange);  color: var(--orange); }

.flow-step:nth-child(4) .flow-num { border-color: var(--brick);   color: var(--brick); }

.flow-step:nth-child(5) .flow-num { border-color: var(--mustard); color: #8a5a08; }

.flow-step-title { font-family: 'Fraunces', Georgia, serif; font-weight: 700; font-size: 9pt; color: var(--coffee); line-height: 1.1; margin-bottom: 0.6mm; }

.flow-step-body  { font-size: 7.4pt; line-height: 1.36; color: var(--coffee); opacity: 0.84; }

Critical rules:



Step circles are outlined, not filled. The full-lesson p5 uses filled step circles; the Number Sheet flow uses outlined. This distinguishes the two visual systems.

Step 0 (prerequisites) is allowed, same as the full-lesson p5 convention. Color cycle starts at rust (step 0).

Connecting vertical hairline runs behind the circles, not in front. flow-num has cream background to mask the line where it passes through.

Step text always title + 1-line body. If the body needs 2 lines, tighten the wording until it fits. Reference: "In Intune admin centre. Policy-based, by team or workload" (1 line).



17.5 Color rules (Number Sheet specific)

The Number Sheet uses the full BvK palette from section 3, but with these specific patterns:

ElementColorBig stat 1 (positive / pricing pop)Mustard #FEA712Big stat 2 (outcome / time saved)Orange #E76219Big stat 3 (cost or volume)Brick #C21717Big stat 4 (trial / favorable)Teal #4a9b95Take-away pop phraseOrange Fraunces 700 (not mustard)Architecture row 1 (Identity / first layer)Brick layer nameArchitecture row 2 (Compute / second layer)Orange layer nameArchitecture row 3 (Operations / third layer)Teal layer nameFlow step circlesCycle rust → teal → orange → brick → mustardHairlines, micro labelsRust + coffee mixNumber unit captionsAlways coffee, never accent

The pop word convention from full-lesson covers (mustard only) does not apply here. The take-away pop in the banner is orange to differentiate. Mustard is reserved for the pricing big-stat — it's the loudest visual moment of the page.

17.6 Header and footer

Header is slim — no big cover hero:



Yeseva 17pt H1 (e.g. "Windows 365 for Agents") with italic "Number Sheet" accent in orange Georgia

Inline italic dek (9pt Georgia rust) separated by a vertical hairline

Meta tracked caps right (V1.0, year, key tags) with a mustard "Public Preview" pill if relevant

Author byline as the last meta segment, in coffee 7.4pt



Footer is the standard BvK footer pattern:



bvk. wordmark left (12pt Bowlby, orange period)

Center: TOPIC · Number Sheet · V1.0 in Fraunces 700 7pt tracked 1.5pt rust

Right: italic disclaimer (7pt Georgia rust at 86% opacity)



No page number on the Number Sheet — it's always one page by definition.

17.7 Content selection (what to include)

A Number Sheet distills a lesson, it doesn't summarize it. Pick:

SlotContentTake-away quoteThe lesson's take-away phrase (from p8 of the full lesson)4 big statsThe 4 most decision-affecting numbers from the lesson (pricing, savings, capacity, trial — whichever apply)5–7 micro-statsSecondary numbers that contextualize the big 4 (limits, supporting figures, related rates)Architecture stackThe 2–4 layers that explain "who delivers what" — typically Identity / Compute / Operations or topical equivalentVertical flowThe 5-step lifecycle / deployment sequence from p5 of the lesson

Don't include:



"Why this lesson" framing — the reader already knows

"Now you try" reflection questions — the reader is referencing, not learning

Long narrative quotes — only the take-away

Multiple case studies — the proof case is good for the lesson but redundant in a number sheet



17.8 Flexibility intent (Number Sheet)

The structure above is the canonical Number Sheet pattern but is not rigid. Adapt freely per topic:

Allowed flexibilityHard rulesNumber of big stats (3–4, never 5+)Fraunces 700 78pt for all big statsNumber of micro-stats (5–7)All micro stats in coffee, never accentArchitecture layer count (2–4)Pure typography only, no card bordersFlow step count (3–6)Outlined step circles, never filledVertical-flow position (right, left, or below)Vertical hairline behind circlesArchitecture position (left or top)Layer name colored by accent cycleWhether to include the take-away bannerIf included, always at the very topCaption length per big-statAll 4 captions bottom-align on the same baseline

When in doubt: render the page, look at it from 60 cm away, and check that the 4 big numbers read instantly. If the eye lands on text first, the page has failed its purpose — the numbers should win.

17.9 Substitutions — when the default recipe doesn't fit

Not every topic has 4 strong numbers, a 3-layer architecture, and a 5-step lifecycle. The principles in 17.2 are non-negotiable, but the components in the default recipe (17.3) can be swapped out for alternatives that serve the same principle on the same real-estate.

The page must still feel like a Number Sheet — one dominant typographic layer, pure typography, no card surfaces, balanced whitespace, BvK palette. Within that, substitute freely.

Common substitutions:

If the topic lacks……replace this component…with this4 distinct hero numbers (only 1–2 dominant figures)Big number wall (4 columns)Hero number pair (2 wide columns, each stat takes 50% width, numerals can grow to 100pt+). Or single mega-number (1 column, numeral can grow to \~150pt) flanked by an italic Georgia framing quote.Any quantitative anchors at allBig number wallPull-quote slab: 1–2 Yeseva-set principle-statements at 36–48pt as the dominant layer. The page becomes a "Principle Sheet" but still scans the same way. (If you reach for this often, the topic is probably better suited to a 1-page lesson summary than a Number Sheet.)A clean 3-layer architecture (more of a hub/spoke or a single-thing-with-properties)Architecture stack (3 typographic rows)Hub-and-spoke list: one center concept at the top of the block + 4–6 properties as labeled rows below. Same typographic conventions (colored Fraunces 11pt key + 8pt body), no card borders.A 5-step lifecycle (work is event-driven, not sequential)Vertical numbered flowTrigger / response table: 2-column grid with Fraunces 700 labels left, 8pt body responses right. Or a state diagram as labeled chips (no boxes — color-coded text with arrows between).A clear before/after comparison the topic requires(no default slot for this)Add a slim comparison band between micro-strip and architecture, 2 columns (Without / With), Fraunces 700 8pt heads, body 8pt. Stays within the no-cards rule by using a single horizontal hairline divider instead of boxes.Both architecture and flow content (very small topic)Architecture + flowReplace both with one wide reference block: a single 2-column typographic key/value list (e.g. "Commands / Effects" or "Roles / Capabilities") that spans the full lower half of the page. Mind the whitespace balance — without two equal-weight blocks the lower half can feel under-filled.

When to abandon the Number Sheet format entirely:

If you find yourself substituting 3 or more components, the topic isn't a Number Sheet candidate. Reach for either:



A full 8-step BvK lesson (storytelling, conceptual, needs the why)

A single-page A4 portrait "Principle Card" (a different format not specified in this document — opens a Yeseva pull-quote + 3 short principle-paragraphs + footer)



The Number Sheet exists because the topic has quantitative density that deserves visual dominance. If it doesn't, force-fitting it makes a worse artifact.

Per-topic creative license:

Beyond substitutions, the following adjustments are always permitted in the name of fit and balance:



Vertical-flow position (right column, left column, below micro-strip as horizontal, or omitted entirely)

Architecture position (lower-left, lower-right, top-row companion to take-away banner)

Take-away banner omission (when the lesson has no quote-able take-away, drop the banner and let the big number wall be the top)

Color slot reassignment (mustard doesn't have to be the pricing pop — assign each accent to whatever role best matches content meaning, then keep that assignment consistent across the page)

Stat ordering left-to-right (most-impactful first vs largest-numeral first vs grouped-by-theme — judgment call)

Footer disclaimer text (specific to the topic: preview-status, regional availability, version-dependence)



When you deviate, the visual rhythm must still feel like a Number Sheet at a glance. Test: lay the page next to the W365 for Agents reference. If it reads as the same family of artifact — same coffee/cream balance, same hairline density, same typographic restraint — the deviation works. If it suddenly feels louder, busier, or more decorative, pull back.

17.10 File naming convention

Nerdio\_<TopicSlug>\_NumberSheet\_BvK.pdf

Examples:



Nerdio\_W365Agents\_NumberSheet\_BvK.pdf (canonical reference)

Nerdio\_AVDHybrid\_NumberSheet\_BvK.pdf

Nerdio\_Compass\_NumberSheet\_BvK.pdf



17.11 Reference output

The canonical rendered example is:

/mnt/user-data/outputs/Nerdio\_W365Agents\_NumberSheet\_BvK.pdf

HTML source:

/home/claude/bvk\_cheat/num\_sheet.html

When in doubt about visual rhythm, alignment, or whitespace balance, compare to this file. It's the source of truth for the Number Sheet variant.



18\. Comparison Sheet variant (landscape A4 side-by-side product compare)

Locked-in May 17, 2026. Born out of the Microsoft Cloud Workspace Comparison Sheet build (AVD vs W365 Enterprise vs W365 Flex vs W365 for Agents).

18.1 Purpose and when to use

The Comparison Sheet is a single-page landscape A4 that puts 3–5 related products, services, or options side-by-side across 8–14 comparison rows. Inspired by Bas's hand-made Cloud Services technology cheat sheet 2.0 (AWS/Azure/GCP), but reskinned in BvK signature without overstating the table-discipline that makes the format work.

Use it when:



The reader's job is to scan differences across competing or related products (cloud platforms, license tiers, deployment models, product editions).

The differences are factual and reasonably stable (pricing, feature support, identity model, scaling behaviour).

A single A4 in landscape is enough to capture the meaningful comparison — not 30+ rows.



Don't use it when:



There are only 2 things to compare (a Comparison Sheet feels empty; use prose or a Number Sheet with a hero-pair).

The "comparison" is really a narrative (use the full 8-step lesson).

The reader doesn't yet know what the products are (a comparison assumes baseline familiarity — teach first, compare second).

The rows would all read "yes / yes / yes" — no differentiation, no need for the format.



18.2 Design principles (these are the rules, always)

These principles transfer across any topic that uses the Comparison Sheet format:



The comparison itself does the work. The structural value of the sheet is the table — rows × columns where the reader's eye scans horizontally across one attribute, or vertically down one product. Everything else (header, footer, decoration) supports that scan, never competes with it.

No card surfaces. No boxes around products, no background fills behind columns, no shadows. The format is a table, not a grid of cards. Hairlines do all the work of separation.

One pop only. A single orange italic in the header title ("Comparison Sheet" accent) and selective bold-orange highlights in body cells for the most-decision-relevant facts. Never multiple pops competing.

Color-coded dot markers for products. A small 2.2mm filled circle in the brand palette (brick / orange / teal / mustard) sits next to each product's Yeseva name in the header row. This replaces logo reinterpretation — Microsoft's official logos stay untouched, BvK style sneaks in through the dots.

Status pills are tag-fills, not buttons. Subtle tinted backgrounds (teal-tint for GA, mustard-tint for Public Preview, brick-tint for Deprecated when needed). No border lines — the pill is identified by colored fill alone, not by an outline. Smaller font (5pt) and tight padding (0.3mm/1.1mm).

Hairlines, not lines. Row dividers, column dividers, and footer separators all use var(--hair-soft) at rgba(106,36,16,0.12). Bold under the header row uses the full var(--coffee) at 1pt for the one structural line that anchors the table.

Always one landscape page. If the content won't fit on one A4 landscape, the topic isn't a Comparison Sheet candidate. Reduce scope (fewer rows, fewer products), don't split across pages.

BvK palette and type system, no substitutes. Cream paper, deep coffee text, the 6-accent palette from section 3.1. Yeseva (product names), Fraunces 700 (row labels, status pills, footer caps), Georgia italic (header dek, footer disclaimer), Bowlby (bvk. wordmark only). Same as full lesson and Number Sheet.



18.3 Layout grid (default recipe)

Page is A4 landscape (297mm × 210mm), body padding 0 12mm (sides) with vertical zones managed by flex layout.

┌──────────────────────────────────────────────────────────────────────────┐

│ 4-color stripe band (2.4mm: teal/mustard/orange/brick)                     │

│                                                                            │

│ HEADER ZONE (\~14mm):                                                       │

│   Yeseva 17pt H1 + italic-orange accent · italic Georgia dek               │

│   Meta tracked caps right + "By Bas van Kaam"                              │

│                                                                            │

│ ─────────────── hairline (var(--hair)) ───────────────                     │

│                                                                            │

│ TABLE ZONE (flex:1):                                                       │

│   ┌─────────┬─────────┬─────────┬─────────┬─────────┐                    │

│   │  LABEL  │ Product │ Product │ Product │ Product │ ← Yeseva 11pt      │

│   │  (42mm) │ ●  GA   │ ●  GA   │ ●  GA   │ ●  PUB  │   + colored dot     │

│   │         │ SUB-LBL │ SUB-LBL │ SUB-LBL │ SUB-LBL │   + tracked sub     │

│   │         │         │         │         │ PREVIEW │   + tinted pill     │

│   │═════════│═════════│═════════│═════════│═════════│ ← 1pt coffee rule  │

│   │ ROW LBL │ body    │ body    │ body    │ body    │ ← 7.4pt / 1.8mm    │

│   │ ROW LBL │ body    │ body    │ body    │ body    │   padding          │

│   │   ...   │   ...   │   ...   │   ...   │   ...   │                    │

│   │ ROW LBL │ body    │ body    │ body    │ body    │ ← 0.4pt hairlines  │

│   └─────────┴─────────┴─────────┴─────────┴─────────┘                    │

│                                                                            │

│ ─────────────── hairline ───────────────                                   │

│                                                                            │

│ FOOTER ZONE (\~10mm, all on one line, vertically centered):                 │

│   bvk.   ·   TITLE · COMPARISON SHEET · V1.0   ·   Disclaimer. URL.       │

└──────────────────────────────────────────────────────────────────────────┘

Column widths:



Label column: 42mm (fixed, accommodates two-line uppercase labels like "STATE / PERSISTENCE")

Product columns: auto (equal-width distribution of remaining \~231mm across 4 columns ≈ 57.75mm each)



18.4 Component specifications

Top stripe band

Same 4-color stripe as full lesson and Number Sheet — teal / mustard / orange / brick, height 2.4mm. Spans full page width.

Header zone

css.head {

&#x20; display: flex;

&#x20; justify-content: space-between;

&#x20; align-items: flex-end;

&#x20; padding: 3mm 12mm 2mm;

&#x20; gap: 8mm;

}

.head-title {

&#x20; font-family: 'Yeseva One', Georgia, serif;

&#x20; font-size: 17pt;

&#x20; color: var(--coffee);

&#x20; line-height: 1;

&#x20; white-space: nowrap;        /\* CRITICAL: title on one line \*/

}

.head-title .sf {

&#x20; font-family: Georgia, serif;

&#x20; font-style: italic;

&#x20; color: var(--orange);       /\* "Comparison Sheet" italic accent \*/

}

.head-sub {

&#x20; font-family: Georgia, serif;

&#x20; font-style: italic;

&#x20; font-size: 9.4pt;

&#x20; color: var(--rust);

&#x20; margin-top: 1mm;

}

.head-meta {

&#x20; text-align: right;

&#x20; font-family: 'Fraunces', Georgia, serif;

&#x20; font-weight: 700;

&#x20; font-size: 7pt;

&#x20; letter-spacing: 1.2pt;

&#x20; text-transform: uppercase;

&#x20; color: var(--rust);

}

.head-meta .author {

&#x20; display: block;

&#x20; margin-top: 1mm;

&#x20; font-size: 8pt;

&#x20; color: var(--coffee);

&#x20; letter-spacing: 0.3pt;

&#x20; text-transform: none;

}

Why title is white-space: nowrap: the header title carries the most editorial weight on the page. If it wraps to two lines, the header zone grows and steals from table zone. Hard rule: one line. If the title is too long to fit at 17pt, reduce to 16pt before wrapping.

Table header row (product cells)

css.ctab thead th {

&#x20; padding: 1.4mm 3mm 2mm;

&#x20; vertical-align: bottom;

&#x20; text-align: left;

&#x20; border-bottom: 1pt solid var(--coffee);

}

.ph-marker {                  /\* The colored dot \*/

&#x20; display: inline-block;

&#x20; width: 2.2mm; height: 2.2mm;

&#x20; border-radius: 99pt;

&#x20; vertical-align: middle;

&#x20; margin-right: 1.4mm;

&#x20; position: relative;

&#x20; top: -0.5mm;                /\* optical alignment with Yeseva baseline \*/

}

.ph-marker.brick   { background: var(--brick); }

.ph-marker.orange  { background: var(--orange); }

.ph-marker.teal    { background: var(--teal); }

.ph-marker.mustard { background: var(--mustard); }

.ph-name {

&#x20; font-family: 'Yeseva One', Georgia, serif;

&#x20; font-size: 11pt;

&#x20; color: var(--coffee);

&#x20; line-height: 1.05;

}

.ph-sub {

&#x20; font-family: 'Fraunces', Georgia, serif;

&#x20; font-weight: 700;

&#x20; font-size: 6.2pt;

&#x20; letter-spacing: 1.2pt;

&#x20; text-transform: uppercase;

&#x20; color: var(--rust);

&#x20; margin-top: 0.8mm;

&#x20; display: flex;

&#x20; align-items: center;

&#x20; gap: 1.2mm;

&#x20; flex-wrap: nowrap;

&#x20; white-space: nowrap;        /\* CRITICAL: sub + pill on one line \*/

}

Status pills (no border — locked May 17, 2026)

css.status-pill {

&#x20; font-family: 'Fraunces', Georgia, serif;

&#x20; font-weight: 700;

&#x20; font-size: 5pt;

&#x20; letter-spacing: 0.9pt;

&#x20; text-transform: uppercase;

&#x20; padding: 0.3mm 1.1mm;

&#x20; border-radius: 99pt;

&#x20; white-space: nowrap;

&#x20; flex-shrink: 0;

&#x20; /\* NO border — only tinted background \*/

}

.status-pill.ga {

&#x20; color: var(--teal);

&#x20; background: rgba(74,155,149,0.16);

}

.status-pill.preview {

&#x20; color: #8a5a08;             /\* deeper mustard for legibility on cream \*/

&#x20; background: rgba(254,167,18,0.22);

}

Critical rule: the original draft used border: 0.4pt solid on pills, which Bas correctly identified as creating a visual "double-rim" effect that looked over-decorated. The locked version removes borders entirely — pills are identified by their tinted fill alone. This also reduces their footprint so the longest pill ("Public Preview") doesn't push against the page edge.

Body cells

css.ctab tbody td {

&#x20; padding: 1.8mm 3mm;

&#x20; vertical-align: top;

&#x20; border-bottom: 0.4pt solid var(--hair-soft);

&#x20; font-size: 7.4pt;

&#x20; line-height: 1.4;

&#x20; color: var(--coffee);

}

.ctab tbody tr:last-child td { border-bottom: none; }

.ctab tbody td.label-c {      /\* Row labels in left column \*/

&#x20; font-family: 'Fraunces', Georgia, serif;

&#x20; font-weight: 700;

&#x20; font-size: 6.8pt;

&#x20; letter-spacing: 1.1pt;

&#x20; text-transform: uppercase;

&#x20; color: var(--rust);

&#x20; padding-left: 0;

&#x20; padding-right: 3mm;

&#x20; vertical-align: middle;

&#x20; white-space: nowrap;

}



/\* Vertical column separators — very subtle \*/

.ctab thead th + th,

.ctab tbody td + td { border-left: 0.4pt solid var(--hair-soft); }

Body emphasis classes:

css.ctab b   { font-weight: 600; color: var(--coffee); }

.ctab i   { font-style: italic; opacity: 0.84; }

.ctab .pop { color: var(--orange); font-weight: 600; }  /\* selective orange pop \*/

.ctab .mut { color: var(--rust); font-style: italic; opacity: 0.84; }

The .pop class is rare — used only when a single phrase in a cell carries genuine "this is the headline of this row" weight (e.g. "Public Preview launch", "Rebrand"). One pop per cell maximum, and not every cell needs one.

Footer zone

css.foot {

&#x20; display: flex;

&#x20; justify-content: space-between;

&#x20; align-items: center;       /\* vertically aligned across mixed fonts \*/

&#x20; padding: 1.8mm 12mm 2.8mm;

}

.wordmark {

&#x20; font-family: 'Bowlby One', sans-serif;

&#x20; font-size: 13pt;

&#x20; color: var(--coffee);

&#x20; letter-spacing: -0.5pt;

&#x20; line-height: 1;

}

.wordmark .dot { color: var(--orange); }

.foot-mid {

&#x20; font-family: 'Fraunces', Georgia, serif;

&#x20; font-weight: 700;

&#x20; font-size: 6.6pt;

&#x20; letter-spacing: 1pt;

&#x20; text-transform: uppercase;

&#x20; color: var(--rust);

&#x20; white-space: nowrap;        /\* one line \*/

}

.foot-mid .sep { color: rgba(106,36,16,0.35); padding: 0 1mm; }

.foot-right {

&#x20; font-family: Georgia, serif;

&#x20; font-style: italic;

&#x20; font-size: 6.6pt;

&#x20; color: var(--rust);

&#x20; opacity: 0.86;

&#x20; white-space: nowrap;        /\* one line including URL \*/

}

Footer structure (HTML):

html<div class="foot">

&#x20; <div class="wordmark">bvk<span class="dot">.</span></div>

&#x20; <div class="foot-mid">Topic Title<span class="sep">·</span>Comparison Sheet<span class="sep">·</span>V1.0</div>

&#x20; <div class="foot-right">Disclaimer text. www.eucnewsnuggets.com</div>

</div>

The URL goes inline at the end of the disclaimer, separated by a single sentence break (period + space). This was Bas's preferred treatment ("simpel — een punt en daar achter de URL"). It keeps the footer to one line, vertically aligned, with the URL functioning as a quiet outbound signal rather than a competing focal point.

18.5 Color rules (Comparison Sheet specific)

The Comparison Sheet uses the full BvK palette from section 3, with this specific assignment for the product markers (4-product layout — adjust for 3 or 5 products by extending the cycle):

ElementColorWhenProduct 1 markerBrick #C21717Typically the most-established / GA-longest productProduct 2 markerOrange #E76219Second tier — well-known, related to product 1Product 3 markerTeal #4a9b95Adjacent product, differentiated modeProduct 4 markerMustard #FEA712Newest / Preview product (matches Preview pill tint)Product 5 marker (if used)Rust #6a2410Fifth in cycleGA status pillTeal text on rgba(74,155,149,0.16) fillAll GA productsPublic Preview status pill#8a5a08 text on rgba(254,167,18,0.22) fillPreview productsDeprecated status pill (if needed)var(--brick) text on rgba(194,23,23,0.14) fillEOL / sunset productsHeader title italic accentOrange Georgia italic"Comparison Sheet" or topic-equivalentBody .pop highlightOrange Fraunces 700Selective key-fact emphasisHairlines (rows + columns)var(--hair-soft) rgba(106,36,16,0.12)All internal table separatorsHeader bottom rulevar(--coffee) 1pt solidThe one structural anchor line

The dot color picks meaning, not visual rotation — match colors to product meaning where possible. For Microsoft Cloud Workspace this happened naturally: brick=AVD (oldest, deepest infra), orange=W365 Enterprise (flagship), teal=W365 Flex (cool/favorable counterpoint), mustard=Agents (newest, preview).

18.6 Content selection

The Comparison Sheet works best with 10–13 rows. Below 8 it feels under-filled; above 14 the layout starts compromising on padding/font and the page loses its breath.

Typical rows for a SaaS/cloud product comparison (pick what differentiates):

RowWhat it capturesBest fitTarget user / scenario in one sentencePricing modelConsumption vs fixed vs per-taskIndicative priceConcrete number with caveat ("verify per region")Session / modePersonal, pooled, dedicated, shared, etc.OS / runtimeWindows versions, Linux support, etc.Management planeWhat admin console / APIIdentity \& licenseWho authenticates + what licenses neededState / persistencePersistent, stateless, mixedScaling modelManual, auto, license-boundHybrid / on-premCloud-only or hybrid pathRegion availabilityWhere it runsDR / resilienceContinuity guaranteesSpecial note (e.g. May 2026 update)Recent material change

Merging tactics when content is dense:



If Identity and License Prereq. overlap heavily across 3+ of the 4 columns → merge into a single "Identity \& license" row.

If Region availability only meaningfully differs for 1–2 products → integrate the differentiator into "Best fit" or "Hybrid" rather than its own row.

If Trial / free info is short → fold it into "Indicative price" as a "30-day free trial" or "50 free hours" addendum.

If Multi-session / Session model overlap → merge with a bold callout in the Session model cell ("Multi-session unique to AVD").

If Image management is similar across most columns → drop the row entirely.



Status pills go on every product in the header sub-row. Use GA for shipping products, Public Preview for preview features, Deprecated/Sunset for products being phased out. If a product has no current status worth noting, the pill can be omitted (and only that one column shows no pill — visual asymmetry is fine when it reflects reality).

18.7 Flexibility intent (within the pattern)

Allowed flexibilityHard rulesNumber of products (3, 4, or 5 columns)Equal-width product columnsNumber of rows (8–14)Body 7.4pt + 1.8mm padding for 10–13 rows; tighten beyond thatColumn label width (38–48mm)Label column always left, Fraunces 700 tracked caps rustRow label wordingAlways single-line via white-space: nowrap — break long ones with / or \&Product marker color cyclePick per content meaning, not rotationPill text (custom statuses)Always tinted fill, no borderHeader sub-label textAlways tracked caps Fraunces 700, max 2 words to fit on one line beside pillHeader title italic accent wordPick a noun ("Comparison Sheet", "Reference Guide", etc.) — always italic orange Georgia

18.8 Substitutions — when the default doesn't fit

If the topic……replace this component…with thisHas 6+ products to compareLandscape 4-product tablePortrait layout: products become inner rows under feature-category groupings. Becomes a different artifact ("Spec Sheet") — consider whether the comparison really needs all 6 in one view.Has only 2 productsThe 4-column comparison structureTwo-column compare with much richer per-cell content, more rows. Or fold into a Number Sheet's hero-pair (section 17.9).Has 1 product with versions across timeSide-by-side compareTimeline strip — single product, columns become versions, rows become features that changed. Same component CSS, different mental model.Has products with no meaningful structural differences (all "yes/yes")Comparison SheetDon't make a Comparison Sheet. Write a full lesson instead.Needs both compare AND detailed feature explanationLandscape compare aloneComparison Sheet plus a 1-page Field Note for the deeper dive — two complementary artifacts, not one overloaded sheet.

Visual test for deviations: lay the deviation next to the Microsoft Cloud Workspace reference. If it reads as the same family — coffee/cream paper, hairlines doing the structural work, one orange italic accent in the header, tinted pills without borders — the deviation works. If it suddenly feels louder, more decorative, or breaks the table-discipline, pull back.

18.9 Density tuning — iteration learnings (May 17, 2026)

The Comparison Sheet's density is the trickiest tuning point. From the Microsoft Cloud Workspace build:



18 rows + 6.6pt body + 1mm padding: technically passable but visually cramped, lines glued together, no breathing room. Avoid.

16 rows + 7pt body + 1.4mm padding: comfortable read, but content was forced to fit (tight cells, last row touching footer). Workable for very dense topics only.

13 rows + 7.4pt body + 1.6mm padding: edge case — fits but last row crowds the footer. One more compromise needed.

11 rows + 7.4pt body + 1.8mm padding: ✅ sweet spot. Comfortable reading, clear hairlines, distinct row rhythm, footer breathes. This is the default to aim for.

8–10 rows: even more breathing room — pad up to 2mm cells if the page feels under-filled, but the visual rhythm is already strong.



Rule of thumb during iteration:



Start with all the rows the topic deserves.

Render and check. If 2+ rows overflow to page 2, find merge candidates (see 18.6 "merging tactics") — don't shrink fonts as the first move.

If 1 row overflows, fine-tune padding (1.8 → 1.6mm) and font (7.4 → 7.2pt) before sacrificing content.

Never go below 7pt body or 1.2mm padding — readability collapses.

If you've merged everything that could be merged and content still doesn't fit, the topic is too big for a Comparison Sheet — split into two.



18.10 File naming convention

Nerdio\_<TopicSlug>\_ComparisonSheet\_BvK.pdf

Examples:



Nerdio\_CloudWorkspace\_ComparisonSheet\_BvK.pdf (canonical reference)

Nerdio\_AVDPlans\_ComparisonSheet\_BvK.pdf

Nerdio\_W365Editions\_ComparisonSheet\_BvK.pdf



For non-Nerdio topics: prefix may be BvK\_ or topic-area (e.g. Identity\_M365vsEntra\_ComparisonSheet\_BvK.pdf).

18.11 Reference output

The canonical rendered example is:

/mnt/user-data/outputs/Nerdio\_CloudWorkspace\_ComparisonSheet\_BvK.pdf

HTML source:

/home/claude/bvk\_cheat/comparison.html

When in doubt about row density, header rhythm, or footer balance, compare to this file. It's the source of truth for the Comparison Sheet variant.



End of specification.

