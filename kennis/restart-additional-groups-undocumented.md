---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [xendesktop, reboot, availability, undocumented]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# The undocumented 'restart additional groups' staggers reboots

How it worked then: the "restart additional groups every:" option in the XenDesktop 7.x restart schedule was poorly documented. You cannot manually divide machines into reboot groups. Instead the system splits machines into two internal groups itself.

Per a Citrix engineer Bas quoted: it reboots only a subset of servers within the Delivery Group so a few machines stay available, waits for the rebooted systems to come back and re-register with the Delivery Controller, then continues rebooting the rest. The intent is to avoid a total application outage during a scheduled restart.

*Bron: blogpost 'How to: Rebooting your XenDesktop 7.x application servers.' (2014-08-19), basvankaam.com.*

## Verwante notities

- [Forcing Microsoft Security Essentials onto Server 2012 (home lab)](mse-on-server-2012-workaround.md)
- [Reboots are a necessary evil; handle them proactively](proactive-over-reactive-ops.md)
