---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [dfs, active-directory, fault-tolerance, storage]
layer: reference
gedateerd: nee
bron: core-knowledge-docs
---

# DFS: Stand-alone vs Domain-based Namespaces

- **Stand-alone**: configuration stored in the host server's local registry. The path starts with the host server name. Only one root target, so not fault tolerant; if the root target is down the whole namespace is inaccessible. Can be made fault tolerant by hosting on a clustered file server.
- **Domain-based**: configuration stored in Active Directory. The path starts with the domain name. Can have multiple root targets, giving fault tolerance and load sharing at the root level.

*Bron: Core Knowledge doc 'DFS Core Doc' (Bas zijn vroege sysadmin-naslag).*

## Verwante notities

- [AD Sites and Replication Topology](ad-sites-and-replication-topology.md)
- [DFS Client Referral Process](dfs-client-referral-process.md)
- [DFS Namespace: Roots, Links, and Targets](dfs-namespace-roots-links-targets.md)
- [Bas's 'one is none' rule for resilience](one-is-none-rule.md)
