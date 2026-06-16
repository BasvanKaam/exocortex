---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [positie, application-delivery, base-image, application-layering]
layer: rich
bron: inside-citrix-fma
---

# Bas on the 'big, bad image' problem

Bas frames the core problem application layering solves as the 'big, bad image.' Applications that can't be virtualised or replaced (e.g. by SaaS) end up baked into your base/production image, which he calls 'Not something to get very excited about.' His hard-won list of cons:

- Apps become harder to maintain and patch: every change must be made on the production image.
- Unused apps still must be shielded/hidden from users, yet still patched and updated.
- Adding/removing apps is 'not dynamic at all.'
- Hard to run multiple versions/editions of the same software.
- Images can grow to hundreds of GBs.
- He has seen apps needing updates weekly or twice-weekly: queuing updates for a biweekly or monthly cycle is unacceptable ('Can you imagine the horror?').
- Each production image change typically triggers a retest/'accept' change protocol that takes a day or two minimum 'and that's fast: trust me!'
- It pushes you toward multiple images/silos per department, when the goal should be 'less is more.'

Alternatives he considers non-ideal but worth weighing: fat clients / persistent desktops, and Reverse-Seamless technology (an app installed on the endpoint, made available inside the virtual session).

## Verwante notities

- [Application layering: abstract the app from the OS](app-layering-abstraction-durable-concept.md)
- [Application delivery: layering vs virtualisation, and AppDisks](application-delivery-layering-vs-virtualisation.md)
- [Three flavours of application delivery in XenDesktop/XenApp](application-delivery-three-flavours.md)
- [Cloud-native does not fix application management](appstream-management-not-solved-positie.md)
- [Bas's key takeaways on application delivery and layering](bas-key-takeaways-application-delivery.md)
- [Bas: only ~50-60% of apps can be virtualised](bas-on-virtualisation-coverage-50-60-percent.md)
- [Bas on the pros of application layering](bas-pros-of-application-layering.md)
- [The 'big bad image' problem: why everything in the base image hurts](big-bad-base-image-problems.md)
- [How application layering works (filter drivers)](how-application-layering-works.md)
- [Bas on MCS, workloads and the case for application layering](mcs-application-workloads-layering.md)
- [Start from a fresh image rather than reusing legacy (Citrix) images](start-from-a-fresh-image.md)
