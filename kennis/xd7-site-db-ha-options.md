---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, sql, high-availability, site-database, mirroring, alwayson]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# HA options for the XD7 Site configuration database

How it worked then. Because the Site SQL database is a single point of failure, Citrix recommended regular backups plus one of these HA approaches:
- **SQL Mirroring** (recommended): failover in seconds, users generally unaffected, but most expensive (full SQL licenses on each server; SQL Express not allowed).
- **Hypervisor HA**: deploy the DB as a VM and use the hypervisor's HA. Cheaper, allows SQL Express, but failover is slower (a new machine must start).
- **SQL Clustering**: one node takes over from a failed one, but more complex to set up and typically slower failover than mirroring.
- **AlwaysOn Availability Groups** (SQL Server 2012): requires SQL instances on WSFC nodes.

*Bron: blogpost 'XenDesktop 7 Site Configuration Database... What about it?' (2013-07-22), basvankaam.com.*

## Verwante notities

- [On over-engineering HA: simplicity often wins, but it all depends](ha-it-all-depends.md)
- ["One is none, two is one" -- but HA is a policy decision, not a dogma](one-is-none-but-it-depends.md)
