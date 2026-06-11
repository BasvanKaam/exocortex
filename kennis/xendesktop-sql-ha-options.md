---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [sql, high-availability, mirroring, clustering, alwayson, vmware]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# SQL HA options for the XenDesktop Site database and when each fits

How it worked then (2013): options to keep the XenDesktop 7 SQL Site database online, roughly in order of fit:

- **SQL Mirroring** — Citrix's first recommendation. Automatic failover in seconds, users generally unaffected. Requires full SQL Server licenses on each node. SQL Express cannot be mirrored. (Note: even then Microsoft had flagged mirroring as deprecated in favor of AlwaysOn, an irony Bas points out in the comments since Citrix still recommended it.)
- **SQL Clustering** — Citrix's second choice. More complex to set up and failover is typically slower than mirroring. Not supported on SQL Express out of the box.
- **AlwaysOn Availability Groups** — SQL Server 2012 Enterprise and later; requires Windows Server Failover Clustering (WSFC) nodes. Microsoft's go-forward HA/DR direction.
- **VMware HA** — does NOT protect the database. It keeps the VM online if a host fails, but is not application-aware, so it has no idea if SQL itself crashed.
- **VMware App HA** (Enterprise Plus) — application-aware, can restart failed components or reset the VM. Supports SQL, but at the time a 1.0 product, complex to set up.
- **VMware Fault Tolerance** — lightning fast live shadow VM, but limited to a single vCPU then, which ruled it out for most SQL servers.
- **Symantec Application HA** — the most enterprise option; 23+ tier-1 apps including custom ones, built on Symantec Cluster Server / Veritas. Separate purchase.

The practical lesson: pick based on what you already license. Companies already running SQL mirroring/clustering or holding VMware Enterprise Plus often have the cheapest path already in hand.

*Bron: blogpost 'XenDesktop SQL High Availability... What to use?!' (2013-12-16), basvankaam.com.*

## Verwante notities

- [On over-engineering HA: simplicity often wins, but it all depends](ha-it-all-depends.md)
