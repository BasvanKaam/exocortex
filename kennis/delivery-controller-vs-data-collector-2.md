---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [delivery-controller, data-collector, fma, ima, zones]
layer: reference
bron: inside-citrix-fma
---

# Delivery Controller vs. Data Collector (FMA vs. IMA)

Delivery Controllers (FMA) are comparable to XenApp 6.5 Data Collectors (IMA): both handle user authentication, resource enumeration and load balancing, but in different ways.

IMA Data Collectors are part of Zones, with exactly one per Zone; multiple Data Collectors means multiple Zones, and they must be able to communicate with each other.

Key architectural differences in the FMA:
- Delivery Controllers do not communicate with each other.
- Session Hosts (VDAs) do not communicate directly with the Central Site database; they register with the Controllers.
- Connection Leasing replaces the role of the LHC (though it was never meant as a replacement).

As of XenDesktop 7.7, Zones returned, but FMA Zones differ architecturally from IMA Zones.

## Verwante notities

- [Citrix IMA Architecture: Data Store and Local Host Cache](citrix-ima-architecture.md)
- [Connection Leasing mechanism](connection-leasing-mechanism.md)
- [Delivery Controller vs Data Collector differences](delivery-controller-vs-data-collector.md)
- [The evolution of the FlexCast Management Architecture](evolution-of-the-fma.md)
- [FMA Controllers differ fundamentally from IMA Data Collectors](fma-vs-ima-controller-differences.md)
- [FMA vs IMA: no Zones, no Data Collectors, no Local Host Cache (2013)](fma-vs-ima-no-zones-no-lhc.md)
- [IMA-to-FMA terminology mapping table](ima-vs-fma-terminology-mapping.md)
- [Zones in the FMA are not the same as IMA 6.5 Zones](zones-fma-vs-ima.md)
