---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [replication, storage, disaster-recovery, clustering]
layer: reference
gedateerd: nee
bron: core-knowledge-docs
---

# Synchronous vs Asynchronous Replication

Data can be replicated at different levels: block (disk device level, by storage controllers or host mirroring), file system (host software), or application (e.g. SQL Server log shipping).

Independent of the level, replication is either:

- **Synchronous**: an operation does not complete until the change is committed at all sites. A block written at site A mirrored to site B only completes once both disks have the change. No data loss, but latency-bound.
- **Asynchronous**: the operation completes as soon as the change lands at the originating site; replication software carries the change to the other site in the background. Faster, but the remote copy may be stale at any point in time.

The choice depends on the application's and business's tolerance for data loss versus latency.

*Bron: Core Knowledge doc 'Clustering Core Doc' (Bas zijn vroege sysadmin-naslag).*

## Verwante notities

- [Active Directory Multimaster Replication](ad-multimaster-replication-fundamentals.md)
- [Azure Files storage redundancy: LRS, ZRS, GRS](azure-files-storage-redundancy-lrs-zrs-grs.md)
- [Cluster Quorum Models](cluster-quorum-models.md)
- [Standard components of a disaster recovery (DR) plan](disaster-recovery-plan-components.md)
- [DNS zone transfer and Notify](dns-zone-transfer-and-notify.md)
- [Geographically Dispersed Clusters](geographically-dispersed-clusters.md)
- [SQL Server 2005 Database Mirroring with a Witness](sql-2005-database-mirroring.md)
