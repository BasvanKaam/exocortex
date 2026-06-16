---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, vda, high-availability, ica, registry]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# VDA high-availability mode for Controller outages

How it worked in XD7. If all Delivery Controllers become unreachable (but the database is fine), a VDA can be configured for high-availability mode, accepting *direct* ICA connections from users instead of broker-mediated ones. It kicks in after a configurable timeout (default 300 seconds) and stays active for at most 30 days while the VDA keeps trying to re-register; once a Controller returns the VDA re-registers without interrupting the user.

Enable it via two manually created registry keys: HighAvailability (1/0) and HaRegistrarTimeout. Users also need a hand-made ICA launch file per user (Citrix doesn't distribute these).

Limitations: dedicated desktops only (not pooled); no user roaming across devices; Controller-originated policies (client drive mapping, clipboard) don't apply and stale policies from a prior registration may persist; affects power-management and NetScaler Gateway/Remote Access scenarios.

*Bron: blogpost 'XenDesktop 7 Site Configuration Database... What about it?' (2013-07-22), basvankaam.com.*

## Verwante notities

- [The Broker Service bundles brokering, XML and STA in one process](citrix-broker-service-three-roles.md)
- [How Local Host Cache works in the FMA](local-host-cache-712-architecture.md)
- [Losing Local Host Cache was a real FMA regression](no-local-host-cache-fma-drawback.md)
- [VDA high-availability mode (direct ICA, last resort)](vda-high-availability-mode.md)
- [Zone VDA registration and failover behaviour (7.7)](zones-vda-registration-failover.md)
