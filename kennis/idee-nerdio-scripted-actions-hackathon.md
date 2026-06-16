---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [idee, hackathon, scripted-actions, community, github, nerdio, avd, open-source]
layer: reference
gedateerd: nee
bron: nerdio-blog
---

# Idea: Nerdio Scripted Actions Community Hackathon

A community scripting contest I designed and ran (first edition 2021, 300+ signups), built around Scripted Actions: get the WVD/AVD/Azure admin community to write PowerShell that solves real day-to-day pain (setup, management, cost optimization), then publish all of it publicly for free. The contest is the engine; the public library is the payoff for the whole community. The mechanics are reusable as a program template for any community build-event, not just a one-off.

## Design principles that make it work
- **Vendor-neutral on purpose.** Scripts do not have to be Nerdio-specific; they should run on native Azure too (host pools, images, MSIX App Attach, Azure Files, FSLogix, any OS/VM). Anything PowerShell-launchable qualifies: Bicep, ARM, JSON, Azure Runbooks, work outside the VM. This widens participation, makes the output useful to everyone, and builds goodwill toward Nerdio. A subset can also flow into the Nerdio Manager Scripted Actions library for customers.
- **Open to anyone, low barrier.** "You do not have to be a master scripter, at all." Reusing your own existing code is fine; it does not have to be brand new. Swag for the first signups.
- **Two levels, judged separately.** Beginner and Advanced, each with their own prizes and rankings. You pick one level and cannot enter both, so newcomers are not crushed by experts.
- **Two categories: Challenges and Freestyle.** Challenges are a curated list of concrete problems; Freestyle is anything that makes a WVD/Azure admin's life easier on time or cost. Both weighted equally, so original ideas score as well as solved challenges (no bonus for picking a challenge over your own idea).
- **Author keeps ownership.** Scripts stay with their creator; the organizer/Nerdio never becomes owner, never resells or reuses entries except as stated. Everyone is credited at the top of their script so authorship is visible. Scripts may later be added to the Nerdio Manager Scripted Actions library, but only with the author's explicit permission.
- **Everything ships publicly.** All entries go to a public GitHub repo, free to download and use, with or without Nerdio installed. The point is shared optimizations, not lock-in.
- **High amplification.** Encourage participants to share on their own channels under a dedicated campaign hashtag, and amplify everything they post in return.

## Scoring
- **Rubric:** usability, originality, functionality, and error/fault-free, max 3 points each.
- **Panel:** named community/MS experts review entries. If a change is needed, the author is asked to agree first.

## Logistics pattern
- Fixed window, kicked off with a recorded launch event a few days before. (First edition ran two full weeks including weekends; a one-week variant including the weekend also works.) Hard submission deadline at a set time/timezone.
- Submit via the public GitHub repo, your own public repo (send the link), or email.
- Each submission needs a clear header describing which challenge it solves (or the Freestyle idea) and proof it ran (short video, screenshot, or code output).

## Topic seeds for inspiration
Performance and cost optimization, image/app management, integrations, AVD/Azure component deployment, monitoring and alerting, MSIX App Attach, security hardening, troubleshooting.

## Related effort
**'100 days of Scripted Actions'** as an ongoing content series, and sharing all Scripted Actions publicly via GitHub rather than only inside the product.

*Bron: Nerdio-content 'SA, GitHub, Hackathon' (Blogs) en 'Hackathon overview doc.docx' (Hackathon).*

## Verwante notities

- [CGIT 'Come Get IT On Tour' as a Community Flywheel](cgit-community-flywheel-on-tour.md)
- [Community Scripts Should Be Free and Vendor-Neutral](community-scripts-should-be-vendor-neutral-and-free.md)
- [Lessons Learned: Running a Community Hackathon](hackathon-lessons-learned-running-a-community-event.md)
- [Idea: crowdsource the Scripted Actions library from the community](idea-community-scripted-actions-library.md)
- [Idea: The self-healing MSP environment](idee-self-healing-msp-environment.md)
- [Nerdio Scripted Actions Hackathon: Bas's Community Event Format](nerdio-scripted-actions-hackathon-concept.md)
- [Community automation should be public and vendor-neutral](positie-community-scripts-publiek-en-vendor-neutraal.md)
- [Scripted-Action Review Rubric (Hackathon judging)](scripted-action-scoring-rubric.md)
