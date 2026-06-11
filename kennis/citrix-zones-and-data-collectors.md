---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [citrix, zones, data-collector, load-balancing, reference, obsolete]
layer: reference
gedateerd: ja
bron: core-knowledge-docs
---

# Citrix Zones and Data Collectors

A farm can contain multiple **zones**; each zone has its own **Data Collector (DC/ZDC)**. All PS servers in a zone share one Data Collector, which holds mostly dynamic data (e.g. load distribution across the zone's servers) in memory.

Each PS reports its own changes to its zone's Data Collector, which in turn relays them to Data Collectors in other zones. The DC is notified immediately on: an ICA session logon/logoff/disconnect/reconnect, a server or application load change, a license change, a PS coming online or going offline, a published application settings change, or a PS IP/MAC address change.

Logon load balancing flow: a user connects to PS1; PS1 contacts another PS (PS2) looking for the DC role; if PS2 is not the DC it contacts the actual DC directly and signals a pending logon; the DC returns the target-server info back through PS2 to PS1, and the user lands on the assigned PS.

Configuration changes from the data store are also pushed to the DC, which relays them to its PS servers (so they update their LHC immediately rather than waiting up to 30 minutes) and to DCs in other zones.

*Bron: Core Knowledge doc 'Citrix General Core Doc' (Bas zijn vroege sysadmin-naslag).*

## Verwante notities

- [Citrix Data Collector Elections](citrix-data-collector-elections.md)
- [Citrix IMA Architecture: Data Store and Local Host Cache](citrix-ima-architecture.md)
- [Citrix Server, Farm and Zone Design Trade-offs](citrix-server-farm-zone-design.md)
- [Delivery Controller vs Data Collector differences](delivery-controller-vs-data-collector.md)
- [FMA Zones: architecture and purpose](fma-zones-architecture-and-purpose.md)
