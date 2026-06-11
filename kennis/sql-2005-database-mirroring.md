---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [sql-server, database, high-availability, mirroring, reference]
layer: reference
gedateerd: ja
bron: core-knowledge-docs
---

# SQL Server 2005 Database Mirroring with a Witness

Reference note on how database mirroring worked, and why it differs from clustering.

A failover cluster does not account for the failure of an individual database; mirroring with a witness server does. The principal and mirror servers, together with the witness, continuously ping each other across three levels: the physical server, the database, and the principal DB.

The mirror server runs continuously in redo mode, so it has little outstanding work when the principal drops out, which makes failover quick. After a failover the database comes out of disconnected state once the redo phase completes, and the roles swap: the old mirror becomes principal and the old principal becomes mirror.

Three operating modes:
- High availability: automatic failover, requires the extra witness hardware.
- High protection: no extra server, manual failover.
- High performance: used when losing a small amount of in-flight data is not critical.

Setup: take a full backup of the DB on the principal, restore it on the mirror, and leave it in NO RECOVERY mode because of the continuous redo phase. The mirror DB must carry the same name as the principal, and the mirror server should be physically identical. SQL logins, SQL Agent jobs and similar must be copied or recreated one-to-one on the mirror.

*Bron: Core Knowledge doc 'SQL 2000, 2005 and 2008 Core Doc' (Bas zijn vroege sysadmin-naslag).*

## Verwante notities

- [High-availability options for the Central Site database](central-site-database-ha-options.md)
- [MSCS Cluster Building Blocks](mscs-cluster-building-blocks.md)
- [SQL Server 2008 Feature Highlights](sql-server-2008-feature-highlights.md)
- [Synchronous vs Asynchronous Replication](synchronous-vs-asynchronous-replication.md)
- [SQL HA options for the XenDesktop Site database and when each fits](xendesktop-sql-ha-options.md)
