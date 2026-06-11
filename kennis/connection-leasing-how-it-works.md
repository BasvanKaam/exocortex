---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [connection-leasing, fma, xenapp, high-availability, ddc]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# How Connection Leasing worked in XenApp 7.6

How it worked then (XenApp/XenDesktop 7.6, enabled by default): each Delivery Controller caches a user's connections to recently used apps/desktops, by default for two weeks. Leases are uploaded to the Site database and synced to other Controllers; each Controller's cache also holds application, desktop, icon and worker (VDA) info on local disk.

If the database becomes unavailable, the Controller enters leased-connection mode and replays cached operations when a user connects or reconnects. Two brief windows reject new sessions/reconnects: right after the DB failure when the DDC enters LC mode, and when it reconnects to the Site database after recovery.

Limitations: supported only for server-hosted apps/desktops and static (assigned) desktops. Not supported for pooled VDI or users with no assigned desktop. Because CL reuses the last cached VDA, load management and session-limit rules may be exceeded.

*Bron: blogpost 'Connection Leasing vs. Local Host Cache. Conclusion? CL doesn't stand a chance!' (2014-10-06), basvankaam.com.*

## Verwante notities

- [The Broker Service bundles brokering, XML and STA in one process](citrix-broker-service-three-roles.md)
- [Connection Leasing is not Local Host Cache, and it's not HA](cl-is-not-lhc-and-not-ha.md)
- [Connection Leasing failover behavior and limitations](connection-leasing-failover-behavior.md)
- [Connection Leasing mechanism](connection-leasing-mechanism.md)
- [What FMA 7.6 changed vs IMA: LHC gone, MCS for servers, Connection Leasing](fma-76-migration-improvements.md)
- [Use LHC over Connection Leasing, and the FMA's modularity proves itself](lhc-over-connection-leasing.md)
- [How Local Host Cache works in the FMA](local-host-cache-712-architecture.md)
- [Losing Local Host Cache was a real FMA regression](no-local-host-cache-fma-drawback.md)
- [New FMA features land in Citrix Workspace Cloud first, then on-prem](positie-zones-and-cloud-first-feature-flow.md)
