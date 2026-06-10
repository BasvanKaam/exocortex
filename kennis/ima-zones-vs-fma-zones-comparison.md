---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [zones, ima, fma, local-host-cache, connection-leasing, delivery-controller]
layer: reference
bron: inside-citrix-fma
---

# IMA Zones vs. FMA Zones comparison

Comparison of Zones between IMA (6.5) and FMA (7.x):

- Core component: Data Collector (IMA) vs. Delivery Controller (FMA).
- Purpose: IMA keeps resources/users close with load balancing and HA; FMA simplifies administration of multiple locations and keeps users close to resources.
- Count: IMA allows max one primary DC per Zone with secondary/backup DCs elected on failure; FMA allows unlimited DCs per Zone (minimum one), all active.
- Resilience: IMA has an LHC on each DC (speeds enumerations, keeps Farm functional when DB is down); FMA uses Connection Leasing (launches certain assigned resources when DB is down).
- DB contact: IMA DC contacts the database every 30 minutes by default; FMA DC has a direct and continuous connection.
- Inter-DC: IMA DCs exchange Zone-related information; FMA DCs do not communicate with each other.
- Load balancing: IMA from the LHC; FMA from the database.
- Registration: IMA has no registration; FMA VDAs register themselves.
- Zone-based policies: IMA has Zone Preference and Load Balancing; FMA has no specific Zone-based policies.
- Best-practice max: 5 Zones (IMA) vs. 10 Zones (FMA).
- Scope: IMA Zones for XenApp only; FMA Zones for both XenApp and XenDesktop.

## Verwante notities

- [Connection Leasing failover behavior and limitations](connection-leasing-failover-behavior.md)
- [Connection Leasing mechanism](connection-leasing-mechanism.md)
- [Delivery Controller vs Data Collector differences](delivery-controller-vs-data-collector.md)
- [FMA Zones: architecture and purpose](fma-zones-architecture-and-purpose.md)
- [IMA-to-FMA terminology mapping table](ima-vs-fma-terminology-mapping.md)
- [Local Host Cache in XenApp 6.5 (IMA)](local-host-cache-ima.md)
- [Bas's Studio and Zones chapter key takeaways](studio-zones-chapter-key-takeaways.md)
- [Zone connection quality limits (bandwidth and RTT)](zone-connection-quality-limits.md)
- [Zones in the FMA are not the same as IMA 6.5 Zones](zones-fma-vs-ima.md)
