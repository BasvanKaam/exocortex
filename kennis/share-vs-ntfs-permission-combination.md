---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [windows, permissions, ntfs, smb, security]
layer: reference
gedateerd: nee
bron: basvankaam-blog
---

# How share and NTFS permissions combine

Share permissions only apply when a folder is accessed over the network. When a user logs in locally to the machine hosting the share, only NTFS permissions apply (or none at all on FAT32). This also holds for RDS / Hosted Shared Desktop sessions.

To find the effective permission on a shared folder accessed over the network:
1. Determine the effective NTFS permission. NTFS works by *least restrictive*: if a user has Read directly but is in a group with Change, the effective NTFS is Change.
2. Determine the effective share permission.
3. Take the *most restrictive* of the two.

Example: Read share + Full Control NTFS yields effective Read. Read NTFS + Full Control share also yields effective Read. The most restrictive of the pair always wins.

Note: Microsoft's effective-permissions tool does not include share permissions in its calculation, only NTFS. Don't use it to reason about share access.

*Bron: blogpost 'A little something about Share vs NTFS permissions' (2013-06-15), basvankaam.com.*

## Verwante notities

- [AD Access Control: Security Descriptors, DACL, SACL](ad-access-control-descriptors.md)
- [Exchange Message Size Limit Precedence](exchange-message-size-limit-precedence.md)
- [Hiding apps (Limit Visibility) vs hiding desktops (PowerShell entitlement filter)](limit-visibility-vs-entitlement.md)
- [Rights vs permissions are not the same thing](rights-vs-permissions-windows.md)
- [Full Control share + lock down with NTFS (and the inheritance trap)](share-permission-best-practice-and-inheritance.md)
- [Share vs NTFS Permissions](share-vs-ntfs-permissions.md)
- [VMFS3 vs VMFS5 block and sub-block sizing](vmfs3-vmfs5-block-sizes.md)
