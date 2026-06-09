# Standaarden

De vaste regels en systemen voor mijn werk: hoe ik schrijf, hoe mijn visuals eruitzien, hoe mijn productie-workflows lopen. Dit bewaakt consistentie over alles wat ik maak.

## De twee assen

Alles hier valt op twee assen. Snap je die, dan snap je de hele map.

**As 1: WAT versus HOE.** Twee losse lagen die samenwerken.
- WAT ik mag zeggen: `schrijfregels/nerdio-content-guard.md`. Nerdio-terminologie, American English, geverifieerde feiten, de never-invent regel.
- HOE ik het zeg: `voice/voice-profile.md`. Ritme, warmte, de route, de register-dial.

De content-guard beperkt de woorden en claims. Het voice-profile bepaalt de stem binnen die grenzen. Voor Nerdio-content draaien ze altijd samen.

**As 2: BvK versus Nerdio.** Twee merken, twee registers, twee visuele skins.
- Voice: volle BvK-stem voor LinkedIn, carousels, podcast en alles wat ik over Nerdio publiceer. Corporate-warmed Nerdio-stem voor officiele Docebo-lessen, courses en formele PPT.
- Visueel: mijn eigen editorial skin (`bvk-pdf-design-system.md`) tegenover de Nerdio-skin (`nerdio-carousel-systeem.md`).

## Wat staat waar

`voice/voice-profile.md`
De volledige schrijfstem uit het 100-vragen interview. Bevat de register-dial (BvK voice versus Nerdio voice), de Eight Engines, de banned-word scan en de hard nos. Lees dit voordat je iets schrijft dat mijn stem draagt. Let op: onderaan staat privecontext, alleen voor calibratie, nooit in publieke output.

`schrijfregels/nerdio-content-guard.md`
De WAT-laag voor alle Nerdio-content. American English, Nerdio-terminologie, live verificatie tegen officiele bronnen, never-invent. Bevat een samenvatting van de belangrijkste regels en verwijst voor de randgevallen naar het volledige stijlboek hieronder.

`schrijfregels/nerdio-style-guide-reference-v3.md`
Het volledige Nerdio L&D-stijlboek (Revision 1, februari 2026). De complete referentie achter de content-guard: lessenstructuur, alle terminologie, punctuatie, hoofdlettergebruik, lijsten. Raadpleeg dit voor randgevallen die de content-guard-samenvatting niet dekt. Bij conflict met de Microsoft Writing Style Guide wint Nerdio L&D.

`visuele-systemen/bvk-pdf-design-system.md`
Mijn eigen PDF-skin. Editorial, anti-corporate, 70s magazine. Coffee/cream/brick/orange/mustard/teal, Bowlby en Yeseva en Fraunces en Georgia. Tagline: Short reads. Sharp takes. No fluff. Voor BvK-carousels en BvK-cheat-sheets (de Comparison Sheet variant staat erin). Footer wijst naar eucnewsnuggets.com.

`visuele-systemen/nerdio-carousel-systeem.md`
De Nerdio-carousel-skin. Navy/teal/lime, Fraunces en Poppins en IBM Plex Mono, Nerdio-logo. A4 portrait vector PDF voor LinkedIn. De bijbehorende template en het render-script staan in `assets/`.

`visuele-systemen/assets/`
Productie-assets bij de Nerdio-carousel: de HTML-template en het Puppeteer render-script.

`workflows/pdf-naar-podcast.md`
Het recept om een microlearning-PDF om te zetten naar een TTS-script voor Finn (Artlist, ElevenLabs V3). Per stap, met de splitsing op 5000 tekens en de human-layer tags.

## Welk register, welke skin

Beslis per kanaal:
- LinkedIn-post, blog, podcast, of een post over Nerdio: volle BvK-stem.
- Officiele Docebo-les, course, formele PPT: Nerdio corporate-warmed.
- Nerdio-carousel als deliverable: Nerdio-skin visueel, maar volle BvK-stem in de tekst (een carousel is een LinkedIn-deliverable).
- Eigen cheat sheet of BvK-carousel: mijn editorial skin.

## Noot over de bestanden

De skills en systemen hier staan ongewijzigd, precies zoals ik ze ook in Claude Code en mijn projecten gebruik. Ze hebben hun eigen kop, dus ze krijgen geen brein-frontmatter erbovenop. Deze README is de index die ze classificeert.
