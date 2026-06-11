---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [windows, permissions, ntfs, inheritance, best-practice]
layer: reference
gedateerd: nee
bron: basvankaam-blog
---

# Full Control share + lock down with NTFS (and the inheritance trap)

A common (though debatable) best practice: grant Full Control share permissions, then use NTFS permissions to lock down access where needed. With Full Control share + Read NTFS, the most restrictive (Read NTFS) applies over the network, and since only NTFS applies locally, Read is enforced no matter how the folder is reached.

The inheritance trap: subfolders inherit the parent's NTFS permissions, not its share permissions. If your effective Read came from Read *share* + Full Control *NTFS*, the root folder stays safe (Read over the network), but subfolders created inside it inherit the Full Control *NTFS* permission. That is exactly what you don't want. Knowing which side of the combination your Read came from matters.

*Bron: blogpost 'A little something about Share vs NTFS permissions' (2013-06-15), basvankaam.com.*

## Verwante notities

- [Rights vs permissions are not the same thing](rights-vs-permissions-windows.md)
- [How share and NTFS permissions combine](share-vs-ntfs-permission-combination.md)
- [Windows user profile versions are incompatible across OS releases](windows-user-profile-version-incompatibility.md)
