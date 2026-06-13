---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [method, ld, instructional-design, nerdio, lab-guide, docebo, template]
layer: reference
gedateerd: nee
bron: nerdio-training
---

# Method: Bas's Nerdio lab-guide template convention

The reusable instructional-design scaffolding he uses for hands-on Nerdio lab guides (Enterprise Foundations and similar). The content click-throughs are disposable; the structure is the durable part.

Document conventions:
- Built from a downloaded .dotx template; you create a new document from it and never edit the template itself. Styles do the heavy lifting; the key to a clean document is using styles, not manual formatting.
- Sentence-style capitalization for all headings and sub-headings: capitalize only the first word and proper nouns.
- Typography: Poppins 11pt for headers/bold (and admonition labels), Open Sans 11pt for body and lab-step text.
- Three reusable building blocks: a Plain table (Table No Outer Borders style), Admonitions (table styled as Important! / Note / Tip), and Lab Steps tables (Lab Steps style, shaded rows in #F5F5F5, rows that do not split across pages).
- A maintained Version History table (date / author / changes) at the front.
- Warns that pasting from another Word doc carries over alien styles; always apply Clear All Formatting to pasted text.

Lab-writing pattern:
- Each lesson is broken into numbered Step 1..N rows, alternating instruction and screenshot placement, with the explicit reminder 'Keep ALL images within the column borders.'
- Every completed section is closed with a 'Section COMPLETE' marker, giving the learner a clear progress beat.
- Steps spell out exactly what to set and what to leave at default (e.g. 'Resource Group = Leave at default', 'VM Size = D2s_v5'), and flag forward dependencies inline ('We'll resize this later when we re-image the hosts').
- Location-aware instructions where it matters (e.g. choose US East or UK South workspace location depending on where the training camp runs).

The instructional principle underneath: standardize on styles and reusable blocks so multiple trainers can co-author consistently, give learners frequent completion checkpoints, and remove ambiguity by stating both the value to change and the values to leave alone.

*Bron: Nerdio-content 'LABGUIDE_Nerdio Enterprise Foundations_v4.0' (Training).*

## Verwante notities

- [Bas's ADDIE course-planning method](addie-course-planning-method.md)
- [Constrain the lab environment so the learning point can't get lost](constrain-the-lab-to-teach.md)
- [Lead enablement with hands-on labs, not slideware](hands-on-labs-over-slideware.md)
- [Idea: 30-day Nerdio engineer bootcamp framework](idee-nerdio-30-day-engineer-bootcamp.md)
- [How Bas designs a self-paced MicroHack lab](microhack-lab-design-method.md)
- [Nerdio Enterprise Optimization Journey (12-step framework)](nerdio-enterprise-optimization-journey.md)
- [The Nerdio training creation framework (Bas's L&D method)](nerdio-training-creation-framework.md)
- [Structure for a 45-minute 'getting started' onboarding session](nmw-getting-started-session-structure.md)
