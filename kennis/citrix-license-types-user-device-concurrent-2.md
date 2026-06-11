---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, licensing, xenapp, xendesktop, flexnet]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Citrix user, device and concurrent licenses

How Citrix XenApp/XenDesktop licensing worked circa 2016 (licensing handled via Flexera's FlexNet, formerly FLEXlm).

**Three forms:** A *user* license = one user, unlimited devices. A *device* license = one device, unlimited users. A *concurrent* license = bound to neither user nor device, consumed for the duration of a session and released on logoff; about twice the price of a user/device license.

**User/device is decided by the server, not you.** You buy 'user/device' licenses (you cannot pre-pick which) and the license server assigns whichever fits based on usage, tracked via device MAC address. Once assigned, a user/device license stays assigned for a minimum of 90 days before check-in (vs concurrent, released at session end). Revoke early with the UDADMIN command-line utility (Bram Wolfs built a GUI around it).

**Mixing:** by default only one type per Site; you cannot mix user/device and concurrent on the same license server. Need both? Use a separate license server. License servers don't talk to each other, so point all production machines at the same one or you'll double-check-out licenses.

**Sizing formula:** user/device licenses needed = A − C + B, where A = total users, B = shared devices, C = users who only ever use shared devices.

**Grace period:** if the license server is unreachable, a 30-day grace period kicks in using locally cached license info (heartbeat every 5 minutes), so no real need for HA on the license server. Since 7.6 there's also a 15-day supplemental grace period allowing unlimited connections when all licenses are in use.

*Bron: blogpost 'Citrix licensing (and Microsoft) demystified? I need your help!' (2016-04-18), basvankaam.com.*

## Verwante notities

- [Formula for sizing user/device licenses](calculating-citrix-license-count-formula.md)
- [Citrix license grace periods and supplemental grace period](citrix-license-grace-periods.md)
- [Citrix license type vs edition vs consumption model](citrix-license-type-vs-edition.md)
- [Citrix Licensing components and FlexNet](citrix-licensing-components-and-flexnet.md)
- [How the license server reassigns user/device licenses](license-server-user-device-reassignment-logic.md)
- [Multi-type licensing in XenDesktop/XenApp 7.14](multi-type-licensing-714.md)
- [How the Citrix license server allocates user/device licenses](user-device-license-server-allocation.md)
