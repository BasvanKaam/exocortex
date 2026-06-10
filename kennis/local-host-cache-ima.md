---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [local-host-cache, ima, data-collector, session-host, fallback]
layer: reference
bron: inside-citrix-fma
---

# Local Host Cache in XenApp 6.5 (IMA)

In a XenApp 6.5 Farm, the Data Collector and all other XenApp servers (except Session Host only servers) have a Local Host Cache (LHC) that caches a copy of the central IMA database. The LHC primarily functions as a fallback for when the IMA database becomes unavailable, but it also speeds up user authentication and application enumeration. Data Collectors also store dynamic live runtime data for load-balancing decisions in their LHC.

All servers (except Session Host only servers, which must be configured explicitly) contact the IMA database (the 'IMA store') every 30 minutes to update their LHC.

Delivery Controllers (FMA) have no LHC, so they always contact the Central Site database for authentication, enumeration and load-balancing data; nothing is stored locally. When Controllers are geographically separated, they all communicate with the same central database, so bandwidth must be planned with the networking team. Note: as of version 7.12 the LHC was renewed and re-introduced into the FMA.

## Verwante notities

- [The Central Site database in the FMA](central-site-database-fma.md)
- [Connection Leasing mechanism](connection-leasing-mechanism.md)
- [Delivery Controller vs Data Collector differences](delivery-controller-vs-data-collector.md)
- [FMA architectural casualties: Zones, LHC and Worker Groups removed then re-added](fma-architectural-changes-zones-lhc-removed.md)
- [FMA Local Host Cache: Principal Broker, Secondary Broker (HA) and CSS](fma-local-host-cache-services.md)
- [IMA-to-FMA terminology mapping table](ima-vs-fma-terminology-mapping.md)
- [IMA Zones vs. FMA Zones comparison](ima-zones-vs-fma-zones-comparison.md)
