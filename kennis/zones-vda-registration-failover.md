---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, zones, vda-registration, connection-leasing, failover, preferred-controller, pvs]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Zone VDA registration and failover behaviour (7.7)

How it worked then: VDAs in a zone register with their preferred Controller (one in their own zone). If none are available, they register with a Controller in the Primary zone, and once registered there they stay registered even after a local Controller returns, there was no fallback mechanism yet (likely because Delivery Controllers don't communicate with each other, unlike Data Collectors in XenApp 6.5). VDAs in the Primary zone can only register with a Primary Site Controller. When a zone Delivery Controller fails, another in the same zone takes over; if none, it auto-fails-over to a Primary Site Controller. Leasing info: Primary Site Controllers store leasing for all zones; satellite-zone Controllers store leasing only for the Primary Site and their own zone. Provisioning Services is NOT zone-aware, configure Machine Catalogs by hand in Studio, otherwise PVS creates them in the Primary zone by default. Keep Machine Catalogs close to the Host Connection they use. Zones depend on Connection Leasing when the central Site database is unavailable.

*Bron: blogpost 'How to configure zones in XenDesktop and XenApp 7.7 plus some extra's!' (2016-01-05), basvankaam.com.*

## Verwante notities

- [How Local Host Cache works in the FMA](local-host-cache-712-architecture.md)
- [VDA high-availability mode for Controller outages](xd7-vda-high-availability-mode.md)
