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
