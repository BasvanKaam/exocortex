name: nerdio-microlesson

description: Build LinkedIn-ready Nerdio microlearning carousels: multi-page A4 portrait vector PDFs with the established Nerdio look-and-feel. Each lesson is typically 6-10 individually designed slides covering one teaching topic, distributed as a swipeable LinkedIn document. Use whenever Bas asks to create a "micro-lesson", "microlearning", "5-minute lesson", "LinkedIn carousel", "PDF carousel", "swipe post", "carousel post", or any single-topic teaching artifact in this format. Trigger phrases include "make a carousel for X", "build a microlesson on X", "build a LinkedIn lesson on X", "turn this topic into a carousel", "another microlearning in the same style", "do for X what we did for Policy Studio". Always produces a multi-page vector PDF, not a single tall page.

Nerdio Microlearning Carousels: A4 portrait, vector PDF

This skill replaces the earlier "tall single-page A4" microlearning format. The current standard is a multi-page A4 portrait vector PDF designed for LinkedIn carousel distribution. Each slide is its own A4 page, individually designed to fill its space, with a consistent design system shared across slides.

The canonical reference for this format is the Intune Policy Studio carousel produced May 2026. That HTML file is the template (microlearning\_carousel\_template.html) and its design tokens are documented below.



MANDATORY: writing layer

This skill governs how the carousel looks. It does NOT govern what the words say.

Before generating ANY slide text — cover title, why-bullets, what-paragraph, pillar bodies, how-step instructions, insight quote, practice scenario, close questions, take-away, footer brand line — load and apply the nerdio-content-guard skill (nerdio\_content\_guard\_SKILL.md).

That skill enforces:



Nerdio L\&D writing style (tone, voice, terminology, capitalization, punctuation, lists, procedures)

American English (color, behavior, organization, specialize, May 8, 2026 — never colour, behaviour, organisation, specialise, 8 May 2026)

Live verification of every technical claim against authoritative sources (Nerdio help docs at nmehelp.getnerdio.com / nmmhelp.getnerdio.com, Microsoft Learn at learn.microsoft.com, the Microsoft Writing Style Guide at learn.microsoft.com/en-us/style-guide, and vendor-specific docs)

The never-invent rule: no claim leaves the workflow without a verified source



This is a non-negotiable step. Do not write a single line of slide content before that skill has been loaded and its pre-writing workflow has been run. Verification happens DURING writing, not at the end as a review pass.

Voice layer (register). nerdio-content-guard governs the words and the claims, it does not set the register. Before generating ANY slide text, also read VOICE\_PROFILE\_Bas\_van\_Kaam\_FINAL.md and write in BvK full voice. A carousel is a LinkedIn deliverable, so it takes full voice, never the corporate-warmed register that is reserved for official Docebo lessons, courses, and formal PPT. The split is clean: nerdio-content-guard governs WHAT you say (terminology, American English, product naming, verified claims), the voice profile governs HOW you explain (rhythm, warmth, comma-stacked cadence, relocate-the-question opens, standing next to the reader). Run the profile's mandatory banned-word scan on every line before output, and load it alongside nerdio-content-guard before writing the first line. No em-dashes.

The visual design tokens, fonts, colors, slide-type vocabulary, layout patterns and iteration recipes documented below are unchanged. They continue to apply exactly as before. The change is purely additive: a writing/content layer running alongside the visual layer.

If nerdio-content-guard is not present in the available skills or project knowledge, flag this to Bas before writing anything — do not fall back to "I'll just verify what I can". The full workflow is required.



When to use this skill

Trigger on any request to build a single-topic teaching artifact for LinkedIn (or similar swipeable distribution). This includes:



"Make a microlesson on Azure Arc"

"Build a LinkedIn carousel on Windows 365 Frontline"

"Turn this topic into a swipe post"

"Same style as the Policy Studio carousel, but for X"

"Do for \[topic] what we did for \[previous topic]"

"Build a 5-min lesson on \[topic]"



Do NOT use this skill for:



Cheat sheets (different format: landscape, denser, multi-section reference)

Slide decks for live presentation (use the pptx skill)

Long-form Word documents (use the docx skill)

Course outlines or ADDIE documents (use the nerdio-content skill)

Single-page reference posters (use canvas-design or build directly)





Output format

Three deliverables per lesson, all in /mnt/user-data/outputs/:



Nerdio\_<TopicSlug>\_MicroLesson\_LinkedIn.pdf: the primary deliverable, multi-page A4 portrait vector PDF for LinkedIn upload

Nerdio\_<TopicSlug>\_MicroLesson\_LinkedIn.html: source HTML (for Bas to edit/iterate locally)

(optional) Nerdio\_<TopicSlug>\_MicroLesson\_cover.png: preview of cover slide for thumbnail/share use



PDF specs:



Page size: A4 portrait (210 × 297 mm)

Margins: zero (the page edges ARE the slide edges, internal padding handles whitespace)

Number of pages: 6-10 typical (the Policy Studio reference has 8). Not strictly fixed.

Render quality: vector PDF only. NEVER bitmap. Renders crisp at any LinkedIn zoom level.

Background: must render gradients, lime accents, colored pills (printBackground:true). If backgrounds disappear, see "Iteration patterns" below.

File size: typically 800 KB - 1.2 MB for 8-slide carousel with embedded logo





Slide-type vocabulary (flexible, not mandatory)

The Policy Studio reference uses an 8-slide structure: Cover, Why, What, Pillars, How, Insight, Practice, Close. Future lessons can vary: pick the slide types that fit the topic. Required: cover slide first, close slide last with takeaway. Everything else is flexible.

The slide types below are reusable building blocks, each with its own CSS class and styling pattern in the template:

cover: slide 1 (always)

Full-bleed dark navy gradient. Contains:



Big Nerdio Manager for Enterprise logo (28mm height)

"EDITION YYYY" tag pill in upper right

"MICROLEARNING" micro-tag with leading line (no time tag — Bas's rule from May 2026 onward; never "MICROLEARNING · 5 MINUTES")

H1 title (68px Fraunces 600, 2 lines)

Italic teal tagline (40px Fraunces italic 500, 1-2 lines)

Author signature ("By Bas van Kaam · Principal Learner Architect")

Page indicator "01 / NN" in mono lower right



A "Swipe →" lime pill on the cover is OPTIONAL. The Policy Studio final removed it. Add only if the topic specifically benefits from the explicit swipe prompt.

why-slide: usually slide 2

Why does this matter for the audience NOW? Three numbered insights (01, 02, 03) with colored numbers (orange/blue/green) and short paragraphs. The H1 above the points uses Fraunces 50px with italic teal accent on a key word and a lime-mark on the punchline phrase.

Lime-mark wrapping exception: the global .lime-mark CSS uses white-space:nowrap to keep highlighted phrases on one line. Sometimes that forces an unnatural line break (e.g. the accent word jumps to its own line, away from the sentence it belongs to). Fix per-instance with an inline override on that specific span: <span class="lime-mark" style="white-space:normal">Full stop</span>. Do NOT modify the global .lime-mark class.

what-slide: defines the concept

H2 in 38px Fraunces, italic intro paragraph in 18px Fraunces, then a "X at a glance" facts block with 5 colored-dot rows (Status, Pricing/Foundation, Coverage, Coexistence/Architecture, Audience/Limits: labels are flexible).

pill-slide: 4-part decomposition

2x2 grid of cells, each with a colored top accent bar (teal, MS-blue, purple, navy). Each cell has a stage label, then 3 sub-points (h4 + p). Use for "the four pillars/mechanics/components of X". For 3-part decomposition, restructure as 1x3 horizontal grid.

Critical content rule: all 12 sub-point <p> items must be 115-145 chars each (3-4 wrap lines). This is what makes the H4 headings align horizontally across cells. Use justify-content:space-around on .pts. Even with that, slight render differences cause \~1-2mm misalignment in some cells. Verify the rendered preview and apply targeted margin-top:-1.5mm ONLY to the cells that visibly sit lower:

css/\* Compass needed: \*/

.pill-slide .cell.c2 .pts,

.pill-slide .cell.c3 .pts { margin-top:-1.5mm; }



/\* AVD Hybrid needed: \*/

.pill-slide .cell.c1 .pts,

.pill-slide .cell.c3 .pts,

.pill-slide .cell.c4 .pts { margin-top:-1.5mm; }

Which cells need the shift varies by content. Always confirm with Bas or check the rendered preview. Don't assume a fixed pattern.

Cell-replacement regex gotcha: when scripting cell content swaps, anchor the regex on the NEXT cell's opening tag, not on closing </div> — non-greedy .\*? matches too early on closing tags.

how-slide: sequence/process timeline

Vertical timeline with numbered badges (0=optional one-off setup, 1-N=runtime steps). Step 0 has dashed border + "ONE-OFF" pill. Steps 1, 2, 3 are progressively colored (teal → blue → purple). Final step uses lime-filled badge to mark the "completion". Connecting dots use 2.5px dashes in muted gray.

insight-slide: the moment of impact (DO NOT DENSIFY)

Full-bleed light gradient (teal-soft → purple-soft → blue-soft). Decorative quote marks in corners (170px Fraunces, opacity 0.18). Centered italic blockquote in 28px Fraunces. This slide is intentionally minimal: when iterating on font sizes for the rest of the lesson, this slide stays untouched. Bas's explicit rule.

practice-slide: worked scenario

Three blocks vertically stacked:



Warm scenario card: orange "TODAY" label + paragraph describing the current pain

Numbers row: 4 big numbers with caps labels (e.g., "320 Employees · 18 Portals · 90 min · 0 APIs")

Teal-blue answer card: "WITH X" label + paragraph + 3 feature chips (✓ Feature) + outcome (big number + small description)



The answer card MUST be filled. Empty space inside the blue card is the most common iteration request. Use feature chips (3 across) to fill the middle area between paragraph and outcome.

Feature chip rules:



Use justify-content:flex-start on .feat (NOT center) so titles align at top regardless of description length. Centering pushes shorter chips down.

Each chip title must be ≤14 chars to fit on one line. Examples that work: "Same console" (12), "Data on-prem" (12), "HCI preserved" (13). "Investment preserved" (20) wraps and breaks alignment across the row.

Body descriptions can be longer; only the title length is constrained.



close-slide: questions + takeaway + CTA (always last)

Three reflection questions (Q · 01, Q · 02, Q · 03) with teal left border, 17px Fraunces titles, italic hints. Below: dark navy take-away band with lime "TAKE-AWAY" label and the lesson's one-line summary in Fraunces 20px (with one bolded lime-green phrase as the visual hook). Below: italic CTA signature + author role line.

diagram-slide: full-page architecture diagram (deviation pattern)

For lessons where a vendor architecture diagram tells the story better than written pillars or a how-timeline. Used in the AVD Hybrid + Nutanix carousel slide 5.

Layout:



Stamp at top

.diagram-frame containing the embedded image (full-width, 3mm padding, 1px border, 6px border-radius). Image is width:100%; height:auto; for responsive scaling.

.diag-section-head: a Fraunces 18px 600 prompt like "Three things this architecture gets right" — frames the cards below.

.diag-insights: 3 horizontal insight cards stacked vertically with justify-content:space-around distribution. Each card:



5px solid colored left accent bar (teal / MS-blue / Nerdio-navy alternating)

30px Fraunces 600 number badge ("01", "02", "03") in the matching accent color

16.5px Fraunces 600 title

13.5px Poppins 1.5 line-height body

6mm/7mm padding





Footer pinned at bottom



The 3 insights translate the diagram's structural concept into architectural takeaways (e.g. "No inbound ports", "One Microsoft control plane", "One management view"). They should NOT just describe the columns of the diagram — that's redundant.

path-slide: learning-path close (deviation pattern, replaces close-slide)

For lessons that wrap into a follow-up training or course track instead of "now you try". Used in the AVD Hybrid + Nutanix carousel slide 8.

Layout:



Stamp + H2 ("Take this further with Nerdio University" style) + brief intro paragraph

.path-cards: 2-card grid. Each card has:



Status badge (lime "AVAILABLE NOW" / amber "IN DEVELOPMENT")

Course title (16px Fraunces 600)

Italic subtitle (11.5px muted)

3 bullets describing coverage (11.5px Poppins)





.path-banner: gradient banner (teal-soft → ms-blue-soft) with "PART OF" label + "the \[Learning Path Name] — more tracks coming soon"

Standard .takeaway band (dark navy, lime accent)

Standard .cta: text-align:center, signature 17px Fraunces italic 500, role 12px caps muted (matches close-slide CTA exactly)

Footer pinned at bottom



Critical CSS fix: .path-slide does NOT have a .body { flex:1 } wrapper like .close-slide does. Without intervention the footer floats mid-page. Add: .path-slide .s-footer { margin-top:auto; } to push the footer down.



Visual specifications (the design system)

These tokens are LOCKED. Do not deviate without explicit user request.

Colors

\--nerdio-navy:      #042838   (primary dark, navigation, takeaway band)

\--nerdio-teal:      #1E9DB8   (primary accent, stamp, lime accents, italic tagline)

\--nerdio-green:     #CDFF4E   (lime, used 1-5% of canvas: lime-mark, takeaway accent, last step badge)

\--nerdio-purple:    #A795C7   (purple accent, pillar 3, step 3 badge)



\--ms-blue:          #0078D4   (Microsoft blue, pillar 2, step 2 badge, brand-dot gradient)

\--ms-blue-soft:     #E5F1FB   (soft blue tint, badge fill, answer card gradient stop)

\--ms-navy:          #003B5C   (deep MS, pillar 4, glance title color)



\--nerdio-teal-soft: #E6F4F7   (soft teal tint, badge fills, answer card gradient stop)



\--ink:              #0B2A3C   (primary text)

\--ink-2:            #2E4256   (body text)

\--muted:            #6B7888   (subtle text, hints, footer brand, timeline dots)

\--line:             #E2E6EE   (separator lines, card borders)

\--paper:            #FFFFFF   (slide background for non-cover slides)

\--warm:             #FFFBED   (scenario card background)

\--warm-line:        #F1D9B6   (scenario card border)

Cover slide gradient (combine three radial glows + linear gradient):

cssbackground:

&#x20; radial-gradient(circle at 18% 20%, rgba(30,157,184,0.42), transparent 55%),

&#x20; radial-gradient(circle at 88% 78%, rgba(0,145,218,0.38), transparent 60%),

&#x20; radial-gradient(circle at 60% 42%, rgba(205,255,78,0.10), transparent 50%),

&#x20; linear-gradient(135deg, #042838 0%, #0A3950 50%, #003B5C 100%);

Insight slide gradient:

cssbackground:

&#x20; radial-gradient(circle at 22% 30%, rgba(30,157,184,0.18), transparent 55%),

&#x20; radial-gradient(circle at 80% 75%, rgba(0,145,218,0.16), transparent 60%),

&#x20; linear-gradient(135deg, #E6F4F7 0%, #ECE6F4 50%, #E1F1FA 100%);

Fonts

Loaded via Google Fonts in <head>:



Body / UI / numbers: Poppins (300, 400, 500, 600, 700, 800)

Display / titles / quote / italic accents: Fraunces (500, 600, 700, italic 500, italic 600)

Mono / code / page numbers / Q-numbers: IBM Plex Mono (400, 500, 600)



Google Fonts URL:

https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,300;0,400;0,500;0,600;0,700;0,800;1,400;1,500\&family=IBM+Plex+Mono:wght@400;500;600\&family=Fraunces:ital,wght@0,500;0,600;0,700;1,500;1,600\&display=swap

Typography sizes (LOCKED: May 2026 standard)

These are the sizes that survived two rounds of "make it bigger" feedback. They are calibrated for LinkedIn carousel readability at thumbnail size. Do not reduce them without explicit user request.

Cover slide:



Logo: 28mm height

EDITION YYYY tag: 12px caps, 2.5px letter-spacing, 6px 14px padding

MICROLEARNING tag: 13px caps, 2.5px letter-spacing

H1 main title: 68px Fraunces 600, line-height 1.04

Italic tagline (em): 40px Fraunces italic 500

Author name line: 15px Poppins

Author title line: 11.5px caps Poppins

Page indicator: 13px IBM Plex Mono



Footer (every non-cover slide):



Height: 18mm, padding 0 18mm, top border 1px var(--line)

Brand text: 12px caps, 0.6px letter-spacing

Brand-dot: 10px circle with teal-blue gradient

Page number: 13px IBM Plex Mono, current page <b> weighted



Section stamp (top of each non-cover slide):



13px Poppins 600 caps, 2px letter-spacing, color teal



Why slide:



H1: 50px Fraunces 500, line-height 1.15. Italic teal accent on 1 word. Lime-mark on punchline.

Number ("01"): 60px Fraunces 700, line-height 1, color per point (orange/blue/green)

Sub-heading (h3): 25px Fraunces 600

Body paragraph: 16px Poppins, line-height 1.55



What slide:



H2: 38px Fraunces 600

Intro: 18px Fraunces italic 500

Glance title: 13px caps Poppins 600, color ms-navy

Facts dt (label + colored dot): 15.5px Poppins 600, dot 10px

Facts dd (description): 15.5px Poppins, line-height 1.55



Pillars slide (2x2 grid):



H2 (centered): 32px Fraunces 600

Cell head (caps label): 12px, 1.6px letter-spacing

Cell sub-heading (h4): 14.5px Fraunces 600

Cell body (p): 12.5px Poppins, line-height 1.5

Cell code: 11.5px IBM Plex Mono

Top accent bar: 3px height

Cell padding: 6mm 6mm



How slide (vertical timeline):



H2: 30px Fraunces 600

Badge size: 18mm circle, font 24px Fraunces 600

Step 0 badge: dashed border 1.5px #B5BDC9, fill #FAFBFD, text #6B7888

Step 1-3 badges: 2px solid colored border, soft tint fill

Step 4 (final) badge: lime #CDFF4E fill, navy border + text

Step heading (h3): 17.5px Fraunces 600

ONE-OFF pill: 11px caps, 1.2px letter-spacing, gray bg

Step body: 14px Poppins, line-height 1.55

Step code: 12.5px IBM Plex Mono

Timeline dots line: 2.5px thick, color #6B7888 (NOT --line: too light), dashes 6px filled / 11px gap



Insight slide (DO NOT MODIFY when iterating):



Stamp: same 13px

Quote (blockquote): 28px Fraunces italic 500, line-height 1.35, max-width 170mm

Bold accent (<b>): non-italic, color teal, weight 600

Decorative quote marks (::before, ::after): 170px Fraunces, opacity 0.18



Practice slide:



H2: 32px Fraunces 600

Scenario label: 12px caps, 1.6px letter-spacing, color #A55613

Scenario p: 14.5px Poppins, line-height 1.55

Number items (.n): 36px Fraunces 700, color #C2620E, white-space: nowrap

Number labels (.l): 12px caps Poppins, color ink-2

Answer label: 12px caps, color teal

Answer p: 14.5px Poppins

Feature chip title: 13.5px Fraunces 600

Feature chip desc: 10.5px Poppins, line-height 1.35

Feature chip check: 20px Fraunces 700, color teal

Outcome big: 36px Fraunces 700, white-space: nowrap (e.g. 25\&nbsp;min)

Outcome small: 13px Poppins, line-height 1.4



Close slide:



H2: 32px Fraunces 600

Q-num (Q · 01): 14px IBM Plex Mono 600, 1.5px letter-spacing, color teal

Q text (qt): 17px Fraunces 600, line-height 1.35

Hint (qh): 13px Poppins italic, color muted; "Hint:" prefix in <b> colored teal

Take-away label: 12px caps Poppins, 2px letter-spacing, color lime

Take-away text: 20px Fraunces 500, line-height 1.4. Bold lime accent on key phrase.

Take-away padding: 9mm 11mm

CTA signature: 17px Fraunces italic 500

CTA role: 12px caps Poppins, color muted



Layout patterns

Page geometry:

┌─────────────────────────────────┐

│  Slide: 210mm × 297mm           │

│  ┌───────────────────────────┐  │

│  │ Top section (flex 0 0)    │  │  padding: 22mm 22mm 0

│  │ stamp + h1/h2             │  │  (or 22mm 18mm for grids)

│  │                           │  │

│  │ Body (flex: 1)            │  │  fills remaining vertical

│  │: content fills space:   │  │  via space-around / space-between

│  │                           │  │

│  └───────────────────────────┘  │

│  ┌───────────────────────────┐  │

│  │ Footer: 18mm (flex 0 0)   │  │  brand-dot + brand text + page num

│  └───────────────────────────┘  │

└─────────────────────────────────┘

Every slide uses display: flex; flex-direction: column. The pattern:

css.slide{

&#x20; width:210mm; height:297mm;

&#x20; display:flex; flex-direction:column;

&#x20; page-break-after:always; break-after:page;

&#x20; overflow:hidden;

}

.slide .top{ flex:0 0 auto; }

.slide .body-or-grid-or-timeline{ flex:1; display:flex; flex-direction:column; justify-content:space-around; }

.slide .s-footer{ flex:0 0 auto; height:18mm; }

This is how slides fill their A4 page. The body content uses flex:1 to take all remaining space, and justify-content: space-around (or space-between) distributes children evenly. Without these, pages end up half-empty (the original problem this design solved).

Page CSS:

css@page{ size:A4 portrait; margin:0; }

Hard rules (the Nerdio brand + Bas's preferences)



No em-dashes (—) anywhere. Replace with period, comma, colon, parentheses, or "and". Non-negotiable Nerdio brand rule.

No bold (<b>) inside flowing prose paragraphs. Latest Bas rule (May 2026). Only keep <b> where it serves a structural function: page numbers (current-page emphasis), author identifier on cover, "Hint:" labels, take-away lime accent, insight quote teal accent. NOT in body paragraphs to emphasize words.

No competitor names. No Citrix, Omnissa, Broadcom, VMware Horizon. Use "legacy on-prem VDI broker" / "your incumbent VDI vendor" / similar neutral phrasing. EXCEPTION: Hyper-V and VMware vSphere allowed in roadmap/hypervisor-listing context (platforms, not direct competitors).

"Nerdio Manager for Enterprise" full name in body prose. "NME" only in compact contexts: diagram callouts, badges, table cells. After first introduction in a slide, "Nerdio Manager" alone is acceptable.

No lesson series numbering, no "Lesson 1 of N", no "Companion to..." Each carousel is a standalone topic. Use "Edition YYYY" tag on the cover.

No links to other lessons. No "Next lesson →" pills.

Lime (#CDFF4E) and purple (#A795C7) are accent-only. Together they should occupy roughly 1-5% of total canvas surface. Never dominant.

The insight slide stays minimal. When iterating on font sizes / page filling for the rest of the carousel, the insight slide is OFF LIMITS. Bas's explicit rule.

A4 portrait, vector PDF, no exceptions. Never produce bitmap PDF (image-based). Use Puppeteer to render HTML directly with printBackground: true.

Targeted edits over full rebuilds. When iterating, change only what's asked. Preserve all other alignment and styling.





Technical accuracy and writing style

Both technical accuracy AND writing style are governed by the nerdio-content-guard skill — see the MANDATORY: writing layer section near the top of this file. Verification happens DURING writing, not as a review pass at the end.

The carousel-specific items that must be verified for every technical lesson (call out to nerdio-content-guard for the full verification protocol):



Step sequences and command paths (e.g., Settings > Environment > Intune)

Role names (e.g., Read Approvals, Manage Approvals)

Pricing figures (per-VM, per-user, per-month rates)

Version numbers (Nerdio Manager 8.0, etc.)

Launch dates, GA dates, preview status

License requirements (E3, E5, E7, etc.)

Capitalization of single technical terms (App Attach vs app attach, Cloud PC vs Cloud pc, etc.)

Acronym expansions on first mention (Azure Virtual Desktop (AVD), Microsoft Intune (Intune), multifactor authentication (MFA))



If a step, term, or fact cannot be verified against an authoritative source (NME Help, NMM Help, Microsoft Learn, Microsoft Writing Style Guide, vendor docs), flag it explicitly to Bas with the closest URL found and a suggested action (confirm / rewrite / drop). Do not bluff technical accuracy. Bas reviews everything before publishing.



Workflow

Step 1: Topic + audience Why

Before touching code, get clear on:



Topic: What single concept is this carousel teaching? (One topic, one lesson: never two)

Audience Why: Why does this matter for an IT admin / EUC engineer / EM-administrator RIGHT NOW? What changed? What's the cost/risk/opportunity?

The hook: A single H1 sentence that makes the audience want to swipe. Use parallel structure ("you can X. you cannot Y.") or dramatic framing.

The 3 numbered insights (slide 2): What's the cost angle (€)? The Microsoft/ecosystem angle (M)? The validation/path angle (✓)? Or three other dimensions appropriate for the topic.

The insight quote: The single sentence the learner walks away with.

The scenario: A concrete worked example (industry, scale, numbers, decision). Should make the reader think "yeah, that's me / my customers".

The take-away: A one-line summary that's quotable. One bolded lime-green phrase as the visual hook.



If Bas hasn't supplied these, ASK before building. Don't guess on the Why: getting that wrong undermines the entire carousel.

Step 2: Slide selection

Decide which slide types from the vocabulary fit this topic. Default 8-slide structure:



cover

why

what

pillars (2x2 four-part decomposition)

how (timeline)

insight

practice

close



Variations seen in practice:



Skip pillars if the topic is more linear than parallel

Add a comparison slide (before/after) before practice

Add a stats/numbers slide if the topic is data-heavy

Use 1x3 horizontal grid instead of 2x2 if 3-part decomposition fits better

6-slide minimum (cover, why, what, insight, practice, close)

10-slide maximum (anything more becomes hard to swipe through)



Step 3: Build from template

Copy microlearning\_carousel\_template.html to working directory. Replace placeholder content. Embed the Nerdio logo as base64 (use nerdio\_logo\_white.png).

bashcp microlearning\_carousel\_template.html policy\_studio\_li\_carousel.html

\# Replace {{LESSON\_TITLE}}, {{COVER\_TITLE\_LINE\_1}}, etc.

\# Embed logo as base64 data URI in src="LOGO\_PLACEHOLDER"

Step 4: Render and verify

Use microlearning\_render\_carousel.js:

bashnode microlearning\_render\_carousel.js my\_lesson.html my\_lesson.pdf

Verify:



Page count matches expected slides

Page size is A4 portrait (594.96 × 841.92 pts)

All gradients and lime accents render (printBackground worked)

No content overflows beyond page edges

Footer is fully visible on every slide (not clipped)

Vector text (selectable in PDF reader, not pixels)



Quick visual check via PNG:

bashpdftoppm -png -r 110 my\_lesson.pdf preview

\# Inspect preview-1.png through preview-NN.png

Step 5: Iterate based on common feedback

See "Iteration patterns" section below. Bas's most common requests:



"Make text bigger" → bump fonts \~15-20% across the lesson, EXCEPT insight slide

"Pages half-empty" → check flex:1 and justify-content: space-around on body containers

"Logo too small" → height 28mm minimum on cover

"Streepje too light" → timeline color #6B7888, thickness 2.5px

"X/Y wraps weirdly" → white-space: nowrap on .lime-mark, on .outcome .big, on number items

"Bold in normal text" → remove all <b> from prose paragraphs (keep structural ones only)



Step 6: Final pass — content guard self-check

By this point, nerdio-content-guard has already verified every technical claim DURING Step 1 (Topic + Why) and DURING content generation in Steps 2-3. Step 6 is the closing self-check, not the primary verification pass.

Run the nerdio-content-guard Step 5 self-check (style + American English + verification confirmation) on every slide one final time. Flag any remaining uncertainty in the response to Bas with source URL and suggested action (confirm / rewrite / drop).

Step 7: Deliver

Save deliverables to /mnt/user-data/outputs/ with consistent naming:



Nerdio\_<TopicSlug>\_MicroLesson\_LinkedIn.pdf

Nerdio\_<TopicSlug>\_MicroLesson\_LinkedIn.html



Use present\_files to surface them. Briefly summarize what was built (slide types used, accuracy verifications done, any flags raised).



Common iteration patterns (proven fixes)

Every pattern below was discovered during real iteration sessions. When a similar issue comes up, jump straight to the fix instead of experimenting.

"Pages are half-empty / lots of whitespace at the bottom"

Check whether the body container of the affected slide is using flex:1 to expand AND justify-content: space-around (or space-between) to distribute children. If body is fixed-size, content sits at the top and bottom is empty. The fix is in the CSS structure, not in adding more content.

"Make all text bigger"

Bump font-sizes across the carousel by \~15-25%. Increase paragraph text first (most readable impact). Headings scale with paragraphs. Maintain the typography hierarchy (H1 > H2 > h3 > h4 > p). If overflow appears after the bump, reduce padding (cell padding 7mm → 6mm → 5mm) before reducing fonts.

Always exclude the insight slide from font-size bumps unless explicitly asked.

"No bold in regular text"

Remove <b> from body paragraphs. Keep <b> where it serves structural function:



Cover author name (<b>Bas van Kaam</b>): identifier

Footer page numbers (<b>04</b> / 08): current-page emphasis

Hint labels (<b>Hint:</b>): structural label

Take-away accent (<b>the brakes you didn't know were missing</b>): visual lime hook

Insight quote accent (<b>the same Intune</b>): visual teal hook (insight slide untouched anyway)



A regex grep grep -n "<b>" file.html shows all current <b> tags for review.

"Streepje too light / not visible"

Timeline dotted line in the how-slide. The default var(--line) (#E2E6EE) is too light for visibility. Change to #6B7888, thickness 2.5px, dashes 6px / 11px gap:

css.how-slide .step:not(:last-child)::after{

&#x20; content:""; position:absolute;

&#x20; left:9mm; top:18mm; bottom:-7mm;

&#x20; width:2.5px;

&#x20; background:repeating-linear-gradient(

&#x20;   180deg, #6B7888 0, #6B7888 6px,

&#x20;   transparent 6px, transparent 11px

&#x20; );

}

"X min should be on one line, not stacked"

Add white-space: nowrap to:

css.practice-slide .num-item .n,

.practice-slide .answer .outcome .big {

&#x20; white-space: nowrap;

}

And use \&nbsp; between number and unit in the HTML (25\&nbsp;min not 25 min).

"Lime mark wraps across two lines / breaks the highlight"

Add white-space: nowrap to .lime-mark. The phrase stays together, even if it forces an earlier line break:

css.lime-mark{

&#x20; background:linear-gradient(180deg, transparent 60%, rgba(205,255,78,0.55) 60%, rgba(205,255,78,0.55) 92%, transparent 92%);

&#x20; padding:0 4px;

&#x20; white-space:nowrap;

}

"Blue answer card on practice slide is mostly empty"

The answer paragraph alone leaves 30-40% of the card empty. Fix: add a .feats grid with 3 feature chips (✓ Auto-backup / ✓ Diff viewer / ✓ 4-eye review) between paragraph and outcome:

html<div class="feats">

&#x20; <div class="feat">

&#x20;   <div class="check">✓</div>

&#x20;   <div class="feat-title">Feature name</div>

&#x20;   <div class="feat-desc">Short reason it mattered</div>

&#x20; </div>

&#x20; <!-- × 3 -->

</div>

CSS:

css.practice-slide .answer .feats{

&#x20; flex:1;

&#x20; display:grid; grid-template-columns:1fr 1fr 1fr; gap:4mm;

&#x20; align-content:center;

}

This pattern: paragraph (flex:0 0 auto) + feats (flex:1) + outcome (flex:0 0 auto) fills the card cleanly.

"Logo barely visible on cover"

height: 28mm minimum. Smaller and it disappears against the gradient.

"Slide 4 (pillars) overflows the page"

Bigger fonts in the cells push content beyond the available space. Fix: remove margin-bottom from .pill-slide .grid. The grid takes all remaining vertical space directly, footer sits naturally below.

"Pillar H4 headings don't line up across cells"

The space-around distribution on .pts is content-length sensitive. Even with all <p> items at 115-145 chars, slight render differences cause \~1-2mm misalignment in some cells. Fix: target the specific cells that visibly sit lower with margin-top:-1.5mm on their .pts. Which cells need it varies by content (Compass needed c2/c3; AVD Hybrid needed c1/c3/c4) — verify on the rendered preview before applying. Don't assume a fixed pattern.

"Path-slide footer floats in the middle of the page"

The .path-slide (learning-path close, deviation pattern) lacks the .body { flex:1 } wrapper that .close-slide has, so the footer ends up wherever the natural flex flow places it. Fix:

css.path-slide .s-footer { margin-top:auto; }

"Diagram-slide is too empty under the architecture image"

After the embedded diagram, the rest of the page can read as half-empty if you only add a caption. Fix: replace the caption with a .diag-section-head ("Three things this architecture gets right" prompt, 18px Fraunces 600) followed by 3 substantial .diag-insights cards distributed via justify-content:space-around. Cards use bigger title/body fonts (16.5px / 13.5px) and a thicker 5px left accent bar than smaller helper cards elsewhere, so they read clearly at LinkedIn carousel scale.

"Backgrounds (gradients, pills, lime accents) disappear in PDF"

This was the cardinal bug in early iterations. Causes:



printBackground: true not set in Puppeteer → set it

CSS overrides like body { background: white !important } interfere with child gradients → don't override

Width mismatch between sheet (1240px) and page (e.g. 327mm = 1236px) → match them, or don't fix sheet width



The current template avoids all three issues. If backgrounds disappear after a CSS change, revert that change first.

"How do I check if my PDF is vector or bitmap?"

Open in PDF reader. If you can SELECT TEXT with the cursor, it's vector. If text is just pixels (cannot select), it's bitmap. Vector renders crisp on LinkedIn; bitmap gets re-rasterized and goes blurry.

You can also check file size: 8-slide vector carousel \~ 900 KB - 1 MB. Same content as bitmap = 1.5-3 MB.

Verifying margins / overflow with PIL

pythonfrom PIL import Image

img = Image.open('preview-N.png')

print(f'page N: {img.size}')

\# Visually inspect to ensure footer fits, no clipped content



Bundled resources (in this skill folder)



microlearning\_carousel\_template.html: Generalized template with {{PLACEHOLDERS}} for topic-specific text. The full Policy Studio carousel structure with all CSS, ready to populate.

microlearning\_render\_carousel.js: Puppeteer script to render the HTML to vector PDF. Run with node microlearning\_render\_carousel.js input.html output.pdf.

microlearning\_policy\_studio\_reference.md: The full Policy Studio lesson as worked example. Use when Bas says "build me one in the same style as Policy Studio".



The template + render script are everything needed to produce a new lesson. Replace placeholders, embed the logo, render.



Trigger examples

User: "Make a 5-min lesson on FSLogix profile containers in the same style as the Policy Studio one"

→ Use this skill. Topic = FSLogix profile containers. Walk Why-first structure with Bas before building.

User: "Build me a microlesson explaining Azure Arc"

→ Use this skill. Topic = Azure Arc fundamentals.

User: "Turn this into a swipe post for LinkedIn"

→ Use this skill. Use the conversation context for topic.

User: "Same look and feel as the Nerdio Policy Studio carousel, but for Windows 365 Cloud PCs"

→ Use this skill. Topic = Windows 365 Cloud PCs.

User: "Build a LinkedIn carousel on Intune Endpoint Privilege Management"

→ Use this skill. Topic = Intune EPM.

User: "Make a cheat sheet on Intune compliance policies"

→ Do NOT use this skill. Different format (landscape, dense reference).

User: "Write a Word doc explaining FSLogix"

→ Do NOT use this skill. Use docx skill.

User: "Build a slide deck for a 30-minute talk on Windows 365"

→ Do NOT use this skill. Use pptx skill.



Anti-patterns (what NOT to do)



Don't produce bitmap PDFs. The original LinkedIn issue was bitmap-stitched PDFs that looked blurry. Always render HTML to vector PDF via Puppeteer.

Don't use exact slide counts as a constraint. 8 slides is the Policy Studio reference. New topics may need 6, 7, 9, 10 slides. Pick what fits the content.

Don't add em-dashes anywhere. Even where they would help readability. Brand rule.

Don't densify the insight slide. Bas's explicit rule. The negative space is the design.

Don't make slide 1 (cover) text-heavy. It's the swipe-or-scroll-past moment. Title + tagline + author. That's it.

Don't put bold on words to emphasize them in body paragraphs. Use color, italic, or restructure the sentence instead.

Don't reduce fonts to fit content. Reduce padding, restructure layout, or trim content. Fonts are calibrated for LinkedIn thumbnail readability.

Don't repeat the same number of slide types you've used before. Mix it up: pillars in one lesson, comparison in another, stats in a third. Variety keeps the format fresh.

Don't reuse exact phrasings between lessons. "Same X. Same Y. Now with Z." is the Policy Studio takeaway pattern. New lesson, new takeaway phrasing.





Version history



May 2026: Format established. Replaces earlier "tall single-page A4" microlearning format. Canonical reference: Intune Policy Studio carousel.

May 2026 (update): Writing/content layer split out into the separate nerdio-content-guard skill. Visual specs unchanged. All slide text now goes through that skill's mandatory pre-writing workflow: Nerdio L\&D style guide, American English, live verification against authoritative sources, never-invent rule. Verification moved from "before finalizing" to "during writing".

May 9, 2026 (update): Cover micro-tag locked to just "MICROLEARNING" (no time tag, applies to every new carousel). Pillars 115-145 char rule made explicit, plus the per-cell margin-top:-1.5mm alignment recipe (content-dependent, verify per carousel). Practice chip title ≤14 chars rule documented. Why-slide lime-mark per-instance white-space:normal override documented. Two new slide-type deviations added: .diagram-slide (architecture image + 3 insight cards, used in AVD Hybrid carousel slide 5) and .path-slide (learning-path close, used in AVD Hybrid carousel slide 8). Three new iteration recipes: pillar H4 alignment, path-slide footer placement, diagram-slide empty-page fix. Topic-specific notes section added (AVD Hybrid burst caveat, Compass screenshot-slide pattern).

June 4, 2026 (update): Voice/register layer added to the MANDATORY writing-layer section. Every carousel now also loads VOICE\_PROFILE\_Bas\_van\_Kaam\_FINAL.md and is written in BvK full voice (a carousel is a LinkedIn deliverable, so corporate-warmed stays reserved for Docebo lessons, courses, and formal PPT). Clean split kept explicit: nerdio-content-guard governs WHAT you say (words, claims, terminology, American English, verified facts), the voice profile governs HOW you explain. Mandatory banned-word scan before output, no em-dashes.





Topic-specific notes (read before writing on these topics)

AVD Hybrid + Nutanix



Burst-to-cloud capability is uncertain. As of May 9, 2026, Bas has flagged that claiming Azure burst capacity for AVD Hybrid + Nutanix is risky because the future capability is not confirmed. Avoid burst claims in scenarios, pillar bullets, training course content, and insight cards for this topic. Use "investment preserved" / "HCI preserved" framing instead.

The Nerdio + Nutanix strategic technology alliance was announced April 7, 2026 at Nutanix .NEXT in Chicago. Public preview in NME 8.0 late May 2026. First non-Azure infrastructure ever supported in NME.

The architecture diagram (Microsoft + Nerdio + Nutanix three planes: on-prem AHV, Azure control plane, Nerdio Manager) works as a .diagram-slide deviation in slide 5.

Wraps into a .path-slide close (slide 8) pointing to "AVD Hybrid Fundamentals" (available on Nerdio University) and "AVD Hybrid Foundational" (in development) as part of the Nerdio Expert Learning Path.



Nerdio Compass



Discovery and migration-readiness tool. Announced May 5, 2026 at NerdioCon. Citrix-first; roadmap covers Microsoft Intune, AVD, Omnissa Horizon (Cloud and Next Gen), and Amazon WorkSpaces.

100-point readiness scoring across 5 destinations (AVD Desktops, AVD RemoteApps, Windows 365, Windows 365 Enterprise mapping, Windows 365 Cloud Apps).

Tier system: green ≥80, amber ≥60, red <60.

4 host modes detected: Multi-random, single-random, single-static discard, single-static local.

HTML and CSV export, plus snapshot comparison over time.

The product UI screenshot deserves a dedicated slide that replaces the standard how-slide. Compass carousel uses a .shot-slide pattern as slide 5: stamp + framed screenshot + caption + 3 small zone cards (top of view / tier legend / bottom table) explaining what to spot in the UI. Cards use space-around distribution and align-content:center so they sit centered between caption and footer.

