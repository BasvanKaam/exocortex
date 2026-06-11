---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, fma, ima, lhc, zones, xendesktop7]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# FMA vs IMA: no Zones, no Data Collectors, no Local Host Cache (2013)

With XenDesktop 7, IMA is gone and FMA takes over. Concretely: Zones and their Zone Data Collectors disappear (it's now one big Site), so no Zone Preference policies, and Load Balance policies apply at Site level. The IMA protocol/service is replaced by the XD7 Delivery Agents. FMA Delivery Controllers have no Local Host Cache, so user authentication, application enumeration, connection requests and server load info all come from the central SQL database (XenDesktop had worked this way for a while).

Bas's design takeaway: because Data Collectors and Zones are gone and every machine behaves as a worker, "most of our old XenApp designs don't apply anymore and it might be time to re-think and re-design them." Note: Citrix later reintroduced an LHC in CVAD, so the 'no LHC' point is specific to this XD7 era.

*Bron: blogpost 'FlexCast Management Architecture' (2013-05-28), basvankaam.com.*

## Verwante notities

- [Citrix policy precedence: IMA vs Citrix AD vs normal AD policies](citrix-policy-precedence-ima-ad.md)
- [Delivery Controller vs. Data Collector (FMA vs. IMA)](delivery-controller-vs-data-collector-2.md)
- [Excalibur merges XenApp and XenDesktop onto FMA](excalibur-merges-xenapp-xendesktop-fma.md)
- [FMA dropped zones and Local Host Cache](fma-no-zones-no-lhc.md)
- [FMA Site database vs IMA store and the missing LHC](fma-site-db-vs-ima-store-lhc.md)
- [FMA Controllers differ fundamentally from IMA Data Collectors](fma-vs-ima-controller-differences.md)
- [IMA-to-FMA terminology: Farm to Site, Data Collector to Delivery Controller](ima-to-fma-terminology-map.md)
- [Losing Local Host Cache was a real FMA regression](no-local-host-cache-fma-drawback.md)
