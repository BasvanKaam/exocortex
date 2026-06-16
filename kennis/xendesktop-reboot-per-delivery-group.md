---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [xendesktop, delivery-group, reboot, fma, operations]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# XenDesktop 7.x reboots are scheduled per Delivery Group

How it worked then (XenDesktop 7.x, 2014): the built-in restart schedule was configured per Delivery Group via Edit Delivery Group > Restart Schedule. You chose daily or a specific weekday and could show a user notification, but the warning interval was fixed to 1, 5 or 15 minutes only.

Because scripts and the built-in feature both target a Delivery Group, you needed a reboot schedule for every Delivery Group in the Site. Design questions to plan for: reboot order (idle machines first), draining sessions, maintenance mode, and keeping a percentage online to avoid total outage.

*Bron: blogpost 'How to: Rebooting your XenDesktop 7.x application servers.' (2014-08-19), basvankaam.com.*

## Verwante notities

- [Reboots are a necessary evil; handle them proactively](proactive-over-reactive-ops.md)
