---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [bas-opinion, application-delivery, base-image, application-layering]
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
