---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, fma, ima, central-site-database, local-host-cache, architecture]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# FMA Site database vs IMA store and the missing LHC

How it worked in the FMA (XenDesktop 7) era. XenApp/IMA kept config in the IMA data store, and every server (except session-host-only 'workers') held a Local Host Cache (LHC), a copy refreshed from the store every 30 minutes, to speed up authentication and app enumeration. Data Collectors additionally held live runtime data for load balancing, organised into zones (one Data Collector per zone).

In the FMA, Delivery Controllers have *no* LHC. They always contact the central Site configuration database (SQL only in XD7) for authentication, app enumeration and load-balance data. There are no zones, just one Site; multiple Controllers spread the load and talk only to the central database and license server, not to each other. Delivery Agents (VDAs) are lighter-weight than full XenApp installs and only talk to the Controllers, never to the database or license server directly.

Consequence: if the Site database becomes unreachable, running sessions keep working but no new sessions can start and no config changes are possible. The central SQL database is a potential single point of failure. (Historical note: the FMA's lack of an LHC was a known limitation in this era and Citrix later reintroduced an LHC mechanism in XenApp/XenDesktop 7.x.)

*Bron: blogpost 'XenDesktop 7 Site Configuration Database... What about it?' (2013-07-22), basvankaam.com.*

## Verwante notities

- [FMA vs IMA: no Zones, no Data Collectors, no Local Host Cache (2013)](fma-vs-ima-no-zones-no-lhc.md)
- [IMA-to-FMA terminology: Farm to Site, Data Collector to Delivery Controller](ima-to-fma-terminology-map.md)
- [Losing Local Host Cache was a real FMA regression](no-local-host-cache-fma-drawback.md)
