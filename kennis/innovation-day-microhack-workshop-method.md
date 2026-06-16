---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [idee, nerdio, microhack, workshop, ldd, facilitation, field-cto]
layer: reference
gedateerd: nee
bron: nerdio-content
---

# Innovation Day MicroHack workshop method

My facilitation pattern for running a Nerdio Innovation Day with hands-on labs, refined across events (Milan and others).

## Opening
Set the frame before touching the tool: today's objectives, how to install Nerdio and the portal, the lab exercise flow, and the general approach. I anchor the general-approach rule with a memorable shorthand: "www" = "while we wait" - the topics we cover live while a long-running task (image build, hostpool create) runs in the background, so dead time becomes teaching time.

## Engagement hooks
Open with a trivia hook to warm the room (e.g. "What was AVD first called?" answers: Windows Virtual Desktop / RDmi / Cowbell). Keep energy with light running gags ("the mailman," "don't be this guy").

## Lab flow (the spine)
The labs always run the same end-to-end EUC build so learners leave having done the full loop:
1. Image import - cover GUI, Resource Rules, settings, Identity / FSLogix, existing AVD.
2. Create Dynamic Hostpool - Scripted Actions (Groups) and UAM.
3. Create Auto-Scale Profile.
4. Apply Auto-Scale Profile - Modeler and User Cost Attribution, hostpool properties.
5. Ongoing image management - Scripted Actions Groups for patch updates, "Set as Image" and "Re-Image" scheduled after Patch Tuesday, the recommendation engine.

## Close with competition
Cap the day with a MicroHack competition (a prize on the line) - a scored build assignment that forces learners to apply everything without hand-holding.

## Pacing principles
- One exercise at a time, in sequence; try to stay in sync as a group but it's not mandatory.
- "Everyone is different." Reassure: "you don't have to do it all perfectly."
- "We are here to help!" - facilitators circulate.
- Safety rail for shared lab tenants: "Be careful. Not sure? ASK!!!"

*Bron: Nerdio-content 'Innovation Day hands-on labs' (Innovation Days).*

## Verwante notities

- [Two event types: Training Camp vs Innovation Day](etc-vs-innovation-day-event-design.md)
- [Idea: Nerdio Fusion - a merged event format](idee-nerdio-fusion-merged-event-format.md)
- [Method: The Learning Pyramid Applied to Technical Training](learning-pyramid-training-method.md)
- [The Innovation Day / MicroHack hands-on event format](nerdio-innovation-day-microhack-format.md)
- [XpressLabs facilitation craft: how Bas runs the room](xpresslabs-facilitation-craft.md)
