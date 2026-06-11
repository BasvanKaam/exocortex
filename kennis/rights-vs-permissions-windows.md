---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [windows, active-directory, group-policy, security]
layer: reference
gedateerd: nee
bron: basvankaam-blog
---

# Rights vs permissions are not the same thing

These two get mixed up constantly. They are different.

- **Rights** are things a user is allowed to *do* on a system. Applied mostly through Group Policy to Organizational Units holding AD objects (user accounts, groups, computer accounts). Examples: system shutdown, install software, log on interactively, log on through Terminal Services, run a batch job.
- **Permissions** apply to objects: files, (shared) folders, printers, shares, registry keys. They are stored in Access Control Lists (ACLs); a single entry is an Access Control Entry (ACE). Prefer assigning to groups of users over single users.

Don't say rights when you mean permissions or vice versa.

*Bron: blogpost 'A little something about Share vs NTFS permissions' (2013-06-15), basvankaam.com.*

## Verwante notities

- [PowerFuse application, file, and IP security (reference)](powerfuse-application-and-file-security.md)
- [Full Control share + lock down with NTFS (and the inheritance trap)](share-permission-best-practice-and-inheritance.md)
- [How share and NTFS permissions combine](share-vs-ntfs-permission-combination.md)
