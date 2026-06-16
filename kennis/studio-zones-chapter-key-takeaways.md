---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [studio, zones, key-takeaways, rtt, local-host-cache]
layer: rich
bron: inside-citrix-fma
---

# Bas's Studio and Zones chapter key takeaways

Bas's own summary list for the Studio/Zones chapter:

- Citrix Studio is THE management console for XenDesktop/XenApp Sites from a single pane of glass, with access to real-time data via the Broker service on the Delivery Controller.
- Studio also offers a range of basic troubleshooting tools.
- Zones are not a new concept, but 7.x Zones are not the same as XenApp 6.5 Zones, not yet anyway. There are distinct differences between the two.
- Citrix is using a phased approach to reintroducing Zones; this is phase one.
- FMA Zones still depend on the Central Site database; there is no LHC.
- The main focus of this first release is to simplify management and keep traffic local.
- Keep an eye on the RTT between Zones; it needs to be below 250 milliseconds, and "less is more." Consult the table for recommended values.

## Verwante notities

- [Citrix Studio: the central management console](citrix-studio-overview.md)
- [FMA Zones: architecture and purpose](fma-zones-architecture-and-purpose.md)
- [IMA Zones vs. FMA Zones comparison](ima-zones-vs-fma-zones-comparison.md)
- [New FMA features land in Citrix Workspace Cloud first, then on-prem](positie-zones-and-cloud-first-feature-flow.md)
- [Citrix Studio console root nodes](studio-console-root-nodes.md)
- [Zone connection quality limits (bandwidth and RTT)](zone-connection-quality-limits.md)
- [Zones in the FMA are not the same as IMA 6.5 Zones](zones-fma-vs-ima.md)
