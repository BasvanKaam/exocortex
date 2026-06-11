---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [citrix, design, farm, zones, wan, reference, obsolete]
layer: reference
gedateerd: ja
bron: core-knowledge-docs
---

# Citrix Server, Farm and Zone Design Trade-offs

Design trade-offs Bas captured for MetaFrame XP/Presentation Server:

**Server placement:** distributing servers across locations keeps sessions close to their data, uses WAN bandwidth efficiently, allows local control, and adds redundancy — but is more complex, may force users to connect to multiple servers, and needs local admins. Centralizing everything is simpler and lets users hit one server for all apps, but data access across a WAN can be slow, bandwidth is wasted forcing remote connections, and it is a single point of failure.

**Farm design:** one large farm gives efficient license usage and a single point of administration but cannot segment admin, requires intra-farm communication across any slow WAN links, and forces all farm-wide settings onto every server. Multiple smaller farms narrow intra-farm communication and allow departmental licensing, local administration, and unrelated configurations — but a user connecting to multiple farms needs multiple licenses, and enterprise-wide changes must be applied per farm.

**Zones:** one zone sends session updates across the WAN only once (to the ZDC) but can slow distant users' logons/queries, may generate more PS-to-ZDC traffic than it saves, and the update traffic cannot be configured/timed/queued/limited. Multiple zones give fast local logons and enumerations but replicate all background info to every ZDC, and every ZDC needs direct access to all other ZDCs.

**Silos:** Citrix servers running only one or a few applications to isolate them from other apps and avoid conflicts.

*Bron: Core Knowledge doc 'Citrix General Core Doc' (Bas zijn vroege sysadmin-naslag).*

## Verwante notities

- [Formula for sizing user/device licenses](calculating-citrix-license-count-formula.md)
- [Citrix Data Collector Elections](citrix-data-collector-elections.md)
- [Citrix IMA Architecture: Data Store and Local Host Cache](citrix-ima-architecture.md)
- [Citrix Zones and Data Collectors](citrix-zones-and-data-collectors.md)
- [FMA Zones: architecture and purpose](fma-zones-architecture-and-purpose.md)
