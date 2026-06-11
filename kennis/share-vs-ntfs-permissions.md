---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [windows, file-server, permissions, ntfs, fundamentals]
layer: reference
gedateerd: nee
bron: core-knowledge-docs
---

# Share vs NTFS Permissions

Two permission layers guard a Windows file share, and they behave differently.

NTFS permissions:
- Only available on an NTFS partition.
- Far more granular than share permissions.
- Apply to individual files and folders, and to subfolders.
- Also apply on local logon, so they still control access when a user signs in directly on the server rather than over the network.

Share permissions:
- Coarse, limited set of rights.
- Apply only to the shared folder itself, not to the files and subfolders beneath it; access to those is governed by NTFS permissions.
- Do nothing for a local logon.

When both apply over the network, the most restrictive of the two wins. NTFS permissions take precedence in the sense that they are the layer that actually controls access to the underlying content; the share is just the gate to reach it.

*Bron: Core Knowledge doc 'Share vs NTFS Core Doc' (Bas zijn vroege sysadmin-naslag).*

## Verwante notities

- [AD Access Control: Security Descriptors, DACL, SACL](ad-access-control-descriptors.md)
- [AD Group Scopes and Replication](ad-group-scopes.md)
- [DFS Namespace: Roots, Links, and Targets](dfs-namespace-roots-links-targets.md)
- [Disk Fragmentation: FAT vs NTFS](fragmentation-fat-vs-ntfs.md)
- [Partitions and File Systems](partitions-and-filesystems.md)
- [PowerFuse application, file, and IP security (reference)](powerfuse-application-and-file-security.md)
- [Full Control share + lock down with NTFS (and the inheritance trap)](share-permission-best-practice-and-inheritance.md)
- [How share and NTFS permissions combine](share-vs-ntfs-permission-combination.md)
