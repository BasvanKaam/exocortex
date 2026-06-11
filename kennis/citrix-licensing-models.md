---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [licensing, flexera, grace-period, ltsr]
layer: reference
bron: inside-citrix-fma
---

# Citrix licensing: user, device and concurrent

Citrix Licensing relies on Flexera software (as do many vendors). The license server is a light role, can share a server, and handles over 10,000 continuous connections.

License types:
- User license: bound to a user, device-independent, allows sessions on unlimited devices.
- Device license: bound to a device, user-independent — any user, one device.
- Concurrent license: not bound to user or device, usable for both, but more expensive.

A user/device license is applied as a token for both XenDesktop and XenApp even if you only use one — they are always issued in pairs. You cannot mix user/device and concurrent licenses within one Site; mixing requires separate Sites and license servers. Licenses are bound to the license server by its case-sensitive local hostname. If the license server is unavailable there is a 30-day grace period during which everything keeps working. NetScaler, unlike XenDesktop/XenApp, needs its license installed directly on the device. Citrix also offers Current Release (CR) and Long Term Service Release (LTSR) tracks; each LTSR gives 5 years mainstream plus 5 years extended support.

## Verwante notities

- [Citrix license grace periods and supplemental grace period](citrix-license-grace-periods.md)
- [Citrix license types: user, device and concurrent](citrix-license-types-user-device-concurrent.md)
- [Citrix Licensing components and FlexNet](citrix-licensing-components-and-flexnet.md)
- [Citrix licensing key facts (Flexera, capacity, NetScaler)](citrix-licensing-key-facts-flexera.md)
- [Citrix LTSR vs Current Release](citrix-ltsr-vs-current-release.md)
- [Credit to Citrix for simplifying NetScaler licensing without a price grab](citrix-simplifying-licensing-praise.md)
- [How the license server reassigns user/device licenses](license-server-user-device-reassignment-logic.md)
- [NetScaler edition licenses and Pay-as-you-Grow](netscaler-adc-edition-licenses-pay-as-you-grow.md)
