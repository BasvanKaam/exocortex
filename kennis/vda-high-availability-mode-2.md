---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-16
tags: [citrix, vda, high-availability, fma, ica, inside-citrix]
layer: reference
gedateerd: ja
bron: inside-citrix-book
---

# VDA high-availability mode (direct ICA fallback)

How it worked in the XenDesktop/XenApp 7.x FMA era. A failsafe for when the SQL database is fine but all Delivery Controllers are unreachable: the VDA can accept direct ICA connections from users instead of brokered ones, so people keep using their desktops and apps.

- Kicks in after all Controller communication fails, following a configurable timeout (default 300 seconds).
- Stays active for a maximum of 30 days total. During this window the VDA keeps trying to register with a Controller; as soon as one returns, registration succeeds without interrupting the user and brokering resumes. If no Controller is found within 30 days, the desktop stops listening and becomes unavailable.
- Enabled via two registry keys created manually after VDA install: `HighAvailability` (1 = on, 0 = off) and `HaRegistrarTimeout` (seconds to keep trying to register before entering HA mode).
- Requires handing each user an ICA launch file for the direct connection; Citrix does not generate or distribute these.
- Per Citrix, suitable only for dedicated desktops where the user-to-VDA mapping is known. Cannot be used with pooled desktops.

Limitations: no user roaming (if the device is already connected, you can't reconnect from a different device); Controller-originated policies (client drive mapping, clipboard access) don't apply because there's no Controller link; stale policies from a previous registration may persist and take effect; NetScaler Gateway / remote access cannot be used.

*Bron: Inside Citrix (2016), 'Inside Citrix ch7 - The Virtual Delivery Agent'.*

## Verwante notities

- [Delivery Controller as the heart of the FMA](delivery-controller-is-heart-of-fma.md)
- [The 'one is none' rule and Delivery Controller high availability](one-is-none-delivery-controller-ha.md)
- [VDA HA mode is a last resort, not a design choice](vda-ha-mode-last-resort.md)
- [VDA high-availability mode (direct ICA, last resort)](vda-high-availability-mode.md)
- [VDA registration and Controller discovery order](vda-registration-and-controller-discovery.md)
- [VDA high-availability mode for Controller outages](xd7-vda-high-availability-mode.md)
