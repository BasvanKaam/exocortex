---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [zones, fma, ima, rtt, design]
layer: rich
bron: inside-citrix-fma
---

# Zones in the FMA are not the same as IMA 6.5 Zones

Bas insists you do not compare FMA-based Zones (7.x) with IMA-based Zones (6.5) — there are distinct differences (he points to a comparison table on page 101). The 7.x Zones are a phased reintroduction, and this is only phase one; the main focus of this first release is simplifying management and keeping traffic local. Critically, Zones in the FMA still depend on the Central Site database — there is no Local Host Cache.

Latency guidance: keep the round-trip time (RTT/RRT) between Zones below 250 ms — less is more. If the RTT to/from a satellite Zone is near or above 250 ms, deploy a separate Site instead (including an SQL HA setup). A registry key can limit the number of brokering requests originating from a satellite Zone. Make sure each Zone's Host Connection is physically close to, or within, that Zone.

## Verwante notities

- [The Central Site database in the FMA](central-site-database-fma.md)
- [Connection Leasing mechanism](connection-leasing-mechanism.md)
- [Delivery Controller vs. Data Collector (FMA vs. IMA)](delivery-controller-vs-data-collector-2.md)
- [FMA architectural casualties: Zones, LHC and Worker Groups removed then re-added](fma-architectural-changes-zones-lhc-removed.md)
- [FMA Local Host Cache: Principal Broker, Secondary Broker (HA) and CSS](fma-local-host-cache-services.md)
- [FMA Zones: architecture and purpose](fma-zones-architecture-and-purpose.md)
- [FMA Zones VDA registration and Controller failover](fma-zones-vda-registration-and-failover.md)
- [IMA Zones vs. FMA Zones comparison](ima-zones-vs-fma-zones-comparison.md)
- [Bas's Studio and Zones chapter key takeaways](studio-zones-chapter-key-takeaways.md)
- [Zone connection quality limits (bandwidth and RTT)](zone-connection-quality-limits.md)
