---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [connection-leasing, delivery-controller, central-site-database, xml, fma]
layer: reference
bron: inside-citrix-fma
---

# Connection Leasing mechanism

Connection Leasing (as of XenDesktop 7.6) was never meant as a replacement for the Local Host Cache; it supplements SQL HA best practices, letting users connect and reconnect to recently used resources even when the Central Site database is unavailable.

When a user successfully launches a resource, the Delivery Controller collects connection-specific info (icons, enumeration, launch info) and sends it to the Central Site database first. Then, in ten-second intervals, it synchronizes to all Delivery Controllers in the Site, where it is saved locally as XML files (the lease information). Each Controller has a direct connection to the database; Controllers do not communicate among each other.

By default each Controller synchronizes up to 1000 leases every 10 seconds until all are synced (configurable via Registry or GPO). On average 2-4 GB of additional disk space suffices. Lease files (~1 KB each) are stored under %programdata%\Citrix\Broker\Cache in subdirectories: Apps, Desktops, Icons, Leases\Enumeration, Leases\Launch, Workers.

- Apps: one file per application per Delivery Group.
- Desktops: one entry per user-assigned VDA (one per VDI user, one per RDSH VDA).
- Icons: one file per unique published resource (one per app, one shared by all desktops).
- Leases\Enumeration: one file per user listing all available resources.
- Leases\Launch: one entry per successfully launched resource, with the machine it started on.
- Workers: one entry per VDA.
