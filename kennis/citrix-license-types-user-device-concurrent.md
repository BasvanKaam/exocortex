---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [citrix, licensing, xendesktop, xenapp, flexnet]
layer: reference
bron: inside-citrix-fma
---

# Citrix license types: user, device and concurrent

Citrix XenApp/XenDesktop licensing distinguishes three license forms. Licensing is handled via Flexera's FlexNet (formerly FLEXlm); this captures how it worked circa 2016.

**Three forms.** A **user license** lets a single user connect from an unlimited number of devices (bound to the user, device-independent). A **device license** lets an unlimited number of users connect from a single device (bound to the device, user-independent). A **concurrent license** sits in between and is tied to neither a specific user nor a machine; one is checked out per active session and checked back in at logoff. A concurrent license costs about twice the price of a user/device license.

**User/device is decided by the server, not you.** You do not choose between user vs device at purchase time. You buy either user/device licenses or concurrent licenses, and for the user/device type the license server decides which one to apply based on usage (tracked via device MAC address). Once assigned, a user/device license stays assigned for a minimum of 90 days before check-in (versus a concurrent license, which is released at session end). You can revoke early with the UDADMIN command-line utility (Bram Wolfs built a GUI around it).

**Mixing.** By default only one type can be used within a XenDesktop Site; user/device and concurrent cannot be mixed on the same license server. If you need both you must set up separate Sites, including separate license servers. License servers do not talk to each other, so point all production machines at the same one or you will double-check-out licenses.

**Sizing formula.** User/device licenses needed = A − C + B, where A = total users, B = shared devices, and C = users who only ever use shared devices.

**Grace period.** If the license server is unreachable, a 30-day grace period kicks in using locally cached license info (heartbeat every 5 minutes), so there is no real need for HA on the license server. Since 7.6 there is also a 15-day supplemental grace period allowing unlimited connections when all licenses are in use.

**Product support.** XenApp (bought separately) only supports concurrent licenses, while XenDesktop supports user, device and concurrent. Buying XenDesktop Enterprise or Platinum includes the use rights to XenApp, so user/device licenses can be used with XenApp — Citrix will not even know the difference.

*Bron: blogpost 'Citrix licensing (and Microsoft) demystified? I need your help!' (2016-04-18), basvankaam.com. Aanvullend: inside-citrix-fma.*
