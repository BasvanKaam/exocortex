---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [citrix-studio, zones, key-takeaways, rtt, local-host-cache]
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
