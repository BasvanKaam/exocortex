---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [clustering, disaster-recovery, replication, high-availability]
layer: reference
gedateerd: nee
bron: core-knowledge-docs
---

# Geographically Dispersed Clusters

A geographically dispersed (stretch) cluster spans sites for site-level resilience:

- Multiple storage arrays, at least one per site, so each site holds a local copy of the data.
- Nodes are wired so that on a site or link failure, the nodes at a site can still reach the storage at that site.
- The storage fabric or host software mirrors/replicates data between sites.

A hard case: two identical sites lose all network and storage links at once. Neither site has enough information to know whether the other will continue, so administrator intervention is required to pick the surviving site. The design goal is to minimize the scenarios that need manual intervention.

*Bron: Core Knowledge doc 'Clustering Core Doc' (Bas zijn vroege sysadmin-naslag).*

## Verwante notities

- [AD Sites and Replication Topology](ad-sites-and-replication-topology.md)
- [Azure high-availability building blocks](azure-high-availability-building-blocks.md)
- [Cluster Quorum Models](cluster-quorum-models.md)
- [Standard components of a disaster recovery (DR) plan](disaster-recovery-plan-components.md)
- [MSCS Cluster Building Blocks](mscs-cluster-building-blocks.md)
- [Synchronous vs Asynchronous Replication](synchronous-vs-asynchronous-replication.md)
