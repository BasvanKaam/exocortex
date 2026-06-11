---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [clustering, mscs, high-availability, windows-server]
layer: reference
gedateerd: ja
bron: core-knowledge-docs
---

# MSCS Cluster Building Blocks

Reference notes on how a classic Windows Server (2003-era) MSCS cluster was put together:

- **Groups / virtual servers** hold **resources** with **dependencies**, governed by **failover / failback policies** and **possible/preferred owners**.
- Each cluster runs under its own **cluster service account**, which needs only local admin, not domain admin.
- The **heartbeat** network has no default gateway or subnet mask and ran at 10 Mbit half duplex on a dedicated interconnect.
- All nodes must use identical hardware and sit in the same subnet.
- Practical hygiene: order the NICs, rename networks to logical names, size the quorum log appropriately, and use **maintenance mode** when servicing a node.

*Bron: Core Knowledge doc 'Clustering Core Doc' (Bas zijn vroege sysadmin-naslag).*

## Verwante notities

- [High-availability options for the Central Site database](central-site-database-ha-options.md)
- [Cluster Quorum Models](cluster-quorum-models.md)
- [Geographically Dispersed Clusters](geographically-dispersed-clusters.md)
- [Bas's 'one is none' rule for resilience](one-is-none-rule.md)
- [SQL Server 2005 Database Mirroring with a Witness](sql-2005-database-mirroring.md)
