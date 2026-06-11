---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [clustering, quorum, mscs, high-availability]
layer: reference
gedateerd: ja
bron: core-knowledge-docs
---

# Cluster Quorum Models

The quorum holds the cluster configuration and arbitrates which nodes form the cluster.

- **Standard (shared disk) quorum**: a ~500 MB quorum disk holding the CLUSDB, checkpoint files, and quorum log. The shared disk is a single point of failure.
- **Majority Node Set (MNS)** quorum: configuration replicated across nodes so the quorum disk is no longer a single point of failure.

In Server 2008/R2 the witness disk approach removed the quorum disk as a single point of failure, and clustering gained GPT disks (>2 TB), IPv6/DNS instead of WINS/NetBIOS, Cluster Shared Volumes for Hy-V migration, a Cluster Validation Tool, and easier setup/migration.

*Bron: Core Knowledge doc 'Clustering Core Doc' (Bas zijn vroege sysadmin-naslag).*

## Verwante notities

- [Citrix Data Collector Elections](citrix-data-collector-elections.md)
- [Geographically Dispersed Clusters](geographically-dispersed-clusters.md)
- [MSCS Cluster Building Blocks](mscs-cluster-building-blocks.md)
- [Synchronous vs Asynchronous Replication](synchronous-vs-asynchronous-replication.md)
