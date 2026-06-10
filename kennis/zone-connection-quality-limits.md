---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [zones, satellite-zones, rtt, bandwidth, sql-ha]
layer: reference
bron: inside-citrix-fma
---

# Zone connection quality limits (bandwidth and RTT)

Because all Delivery Controllers must constantly read/write to the Central Site database, the link quality between satellite and primary Zones is limited. The number of VDAs and user sessions in a satellite Zone determines the minimum bandwidth and RTT needed.

FMA fact: if the RTT to/from a satellite Zone is near or above 250 ms, a separate Site deployment (including its own SQL HA setup) is advised.

Citrix's recommended connection quality limits (supported sessions / session launches / minimum bandwidth / max RTT):
- < 50: 20 launches / 1 Mbps / 250 ms
- 50-500: 25 / 1.5 Mbps / 100 ms
- 500-1000: 30 / 2 Mbps / 50 ms
- 1000-3000: 60 / 8 Mbps / 10 ms
- > 3000: 60 / 8 Mbps / 5 ms

Zone naming: a primary Zone always exists (named 'primary' by default, changeable) plus optional satellite Zones. Names must be unique within the Site; spaces are allowed but special characters are not. Delegated administration can be scoped to managing Zones. Studio (and Director) is configured only in the primary Zone and can be published to other Zones.

## Verwante notities

- [High-availability options for the Central Site database](central-site-database-ha-options.md)
- [FMA Zones: architecture and purpose](fma-zones-architecture-and-purpose.md)
- [FMA Zones VDA registration and Controller failover](fma-zones-vda-registration-and-failover.md)
- [IMA Zones vs. FMA Zones comparison](ima-zones-vs-fma-zones-comparison.md)
- [Bas's Studio and Zones chapter key takeaways](studio-zones-chapter-key-takeaways.md)
- [Zones in the FMA are not the same as IMA 6.5 Zones](zones-fma-vs-ima.md)
