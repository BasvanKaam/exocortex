---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [idee, microhack, method, enablement, hands-on-labs, instructional-design, addie]
layer: reference
gedateerd: nee
bron: nerdio-content
---

# How Bas designs a self-paced MicroHack lab

Reusable instructional pattern behind Bas's NME MicroHacks, independent of the specific product version. The lab is a chain of self-paced exercises that together complete one realistic end-to-end workflow rather than a set of disconnected feature demos.

**The structure of every exercise:**
1. **Introduction** - a few sentences of plain-language context: what the feature is, why it exists, and how it connects to the previous and next exercises.
2. **Challenge** - a precise, parameterized task list (exact names, sizes, values to enter). Specific enough that attendees act without guessing, open enough that they have to navigate the product themselves.
3. **Success Criteria** - observable, checkable outcomes ('you should see X', 'a clock icon appears', 'costs around $5/user'). Lets attendees self-verify and signals when to call a facilitator over.
4. **Learning Resources** - links to the official docs for that exact feature, so the lab doubles as a guided tour of the documentation.

**Design principles Bas applies:**
- **One continuous storyline.** Each exercise builds on the artifact from the last (the resource rule constrains the image import; the image feeds the host pool; the autoscale profile gets applied to that host pool). Attendees finish having built one coherent environment, not seven throwaways.
- **Constrain to teach.** Early exercises deliberately lock down choices (e.g. a resource rule that leaves only four VM sizes and one image) so later steps can't go off the rails and the learning point lands cleanly.
- **Parallelize the waiting.** Long-running operations (image import) are kicked off, then 'while we wait, we move on to the next exercise' - dead time becomes progress.
- **Facilitator checkpoints.** Recurring 'have us check the result' beats keep a self-paced lab from silently drifting, without turning it into instructor-led.
- **Concrete numeric targets** as success criteria (cost savings near 80%, per-user cost around a target figure) give attendees a clear 'did it work' signal and reinforce the product's value at the same time.

*Bron: Nerdio-content 'Microhack' (Microhack ideas).*

## Verwante notities

- [Method: Bas's Nerdio lab-guide template convention](method-nerdio-lab-guide-template.md)
- [Nerdio Fusion: a hybrid vision + skill event concept](nerdio-fusion-hybrid-event-concept.md)
