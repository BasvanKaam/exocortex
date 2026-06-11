---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [dfs, referral, client, storage]
layer: reference
gedateerd: nee
bron: core-knowledge-docs
---

# DFS Client Referral Process

High-level flow when a client accesses a DFS namespace:

1. Client contacts the DFS namespace (or a link folder within it).
2. A domain controller returns a referral listing the root target servers.
3. The client picks the first root server in the list and queries for available link targets.
4. The client connects to the first link target in the list.
5. The data is displayed.

The referral model is what lets DFS hand clients an ordered list of targets to fail over between.

*Bron: Core Knowledge doc 'DFS Core Doc' (Bas zijn vroege sysadmin-naslag).*

## Verwante notities

- [AD Sites and Replication Topology](ad-sites-and-replication-topology.md)
- [DFS Namespace: Roots, Links, and Targets](dfs-namespace-roots-links-targets.md)
- [DFS: Stand-alone vs Domain-based Namespaces](dfs-standalone-vs-domain-based.md)
- [NetScaler GSLB is DNS-based multi-site traffic management](netscaler-gslb-dns-foundation.md)
- [StoreFront Multi-Site aggregation, mapping and failover](storefront-multisite-aggregation.md)
