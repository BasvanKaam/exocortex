---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [dfs, storage, file-services, windows-server]
layer: reference
gedateerd: nee
bron: core-knowledge-docs
---

# DFS Namespace: Roots, Links, and Targets

DFS presents a virtual view of shared folders living on different servers under one logical tree.

- **Namespace**: the virtual view as a whole, built from a root plus links and targets.
- **Root**: the starting point of the namespace. Maps to one or more root targets, each a shared folder on a separate server. Must reside on an NTFS volume. Form: `\\servername\rootname` or `\\domainname\rootname`.
- **Root target**: a physical server hosting the namespace.
- **Link**: a component below the root that maps to one or more link targets.
- **Link target**: the destination of a link, any UNC path (a shared folder or even another DFS path).
- **DFS path**: any UNC path starting with a DFS root.

*Bron: Core Knowledge doc 'DFS Core Doc' (Bas zijn vroege sysadmin-naslag).*

## Verwante notities

- [DFS Client Referral Process](dfs-client-referral-process.md)
- [DFS: Stand-alone vs Domain-based Namespaces](dfs-standalone-vs-domain-based.md)
- [NAS vs SAN Storage Architectures](nas-vs-san-storage.md)
- [Share vs NTFS Permissions](share-vs-ntfs-permissions.md)
