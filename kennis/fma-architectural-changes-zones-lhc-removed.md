---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [fma, zones, local-host-cache, worker-groups, architecture, war-story]
layer: rich
bron: inside-citrix-fma
---

# FMA architectural casualties: Zones, LHC and Worker Groups removed then re-added

When XenApp joined the FMA in 2013, Bas notes fundamental architectural changes, some permanent, some not:

- Up to XenDesktop/XenApp 7.6, Zones were not just non-optional, they were gone altogether. All you had were separate complete Sites, each needing a mandatory HA SQL setup, 'not ideal.'
- No more Zone preference (failover) policies, no Local Host Cache (LHC); Load Balance policies were applied at Site level.
- Worker Groups were 'taken from us as well.'
- Version 7.7 reintroduced Zones (but still no Worker Groups, no LHC at that point), and Bas warns these new Zones work differently from XenApp 6.5 Zones.
- Power management, especially from a XenApp perspective, was 'still far from ideal even within 7.8.'
- Permanently gone: the IMA protocol and service, replaced by VDAs installed on session hosts, a much more lightweight approach than the IMA (where XenApp was basically installed on each system), even lighter than XenApp 6.5 'Session only mode'.

2018 update he adds: Local Host Cache has since been re-added. His characteristic aside: 'Oh, and did I mention that Worker Groups were taken from us as well?'

## Bron-citaten (NL, verbatim)

> Oh, and did I mention that Worker Groups were taken from us as well?

## Verwante notities

- [Delivery Controller vs Data Collector differences](delivery-controller-vs-data-collector.md)
- [The evolution of the FlexCast Management Architecture](evolution-of-the-fma.md)
- [FMA Local Host Cache: Principal Broker, Secondary Broker (HA) and CSS](fma-local-host-cache-services.md)
- [FMA Zones: architecture and purpose](fma-zones-architecture-and-purpose.md)
- [Local Host Cache in XenApp 6.5 (IMA)](local-host-cache-ima.md)
- [XenApp folded into the FMA: the Excalibur / XenDesktop 7.0 moment](xenapp-joins-fma-excalibur-2013.md)
- [Zones in the FMA are not the same as IMA 6.5 Zones](zones-fma-vs-ima.md)
