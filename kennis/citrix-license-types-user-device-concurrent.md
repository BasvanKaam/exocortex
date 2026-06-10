---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [citrix, licensing, xendesktop, xenapp]
layer: reference
bron: inside-citrix-fma
---

# Citrix license types: user, device and concurrent

Citrix licenses come in three forms. A **user license** lets a single user connect from an unlimited number of devices (bound to the user, device-independent). A **device license** lets an unlimited number of users connect from a single device (bound to the device, user-independent). **Concurrent licenses** sit in between and are not tied to a specific user or machine; one is checked out per active session and checked back in at logoff.

You do not choose between user vs device at purchase time — you buy either user/device licenses or concurrent licenses, and for the user/device type the license server decides which one to apply. By default only one type can be used within a XenDesktop Site; user/device and concurrent cannot be mixed. If you need both you must set up separate Sites, including separate license servers.

Product support differs: XenApp (bought separately) only supports concurrent licenses, while XenDesktop supports user, device and concurrent. Buying XenDesktop Enterprise or Platinum includes the use rights to XenApp, so user/device licenses can be used with XenApp — Citrix won't even know the difference.

## Verwante notities

- [Citrix license grace periods and supplemental grace period](citrix-license-grace-periods.md)
- [Citrix Licensing components and FlexNet](citrix-licensing-components-and-flexnet.md)
- [Citrix licensing key facts (Flexera, capacity, NetScaler)](citrix-licensing-key-facts-flexera.md)
- [Citrix licensing: user, device and concurrent](citrix-licensing-models.md)
- [Startup license and the license checkout process](citrix-startup-license-and-checkout.md)
- [How the license server reassigns user/device licenses](license-server-user-device-reassignment-logic.md)
- [Microsoft RDS CALs and the XenApp vs XenDesktop split](microsoft-rds-cals-with-xenapp.md)
