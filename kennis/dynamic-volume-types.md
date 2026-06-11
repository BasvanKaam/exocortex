---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [storage, dynamic-disks, raid, volumes, windows-2000]
layer: reference
gedateerd: ja
bron: core-knowledge-docs
---

# Dynamic Volume Types

Volume types available on dynamic disks (with their NT 4.0 partition-based predecessors in brackets):

- **Simple volume**: space from a single disk; can be extended within that disk. Not fault tolerant, but can be mirrored.
- **Spanned volume** [volume set]: space from more than one disk, concatenated; can be extended any time. Not fault tolerant, cannot be mirrored.
- **Striped volume** [stripe set]: data written in stripes across two or more disks. Best read/write performance of all Windows 2000 volumes, but not fault tolerant - one disk failure loses the whole volume. Cannot be mirrored or extended. (RAID 0.)
- **Mirrored volume** [mirror set]: duplicates data across two disks for redundancy; survives one disk failure. Slower than RAID 5 on reads but faster on writes. (RAID 1.)

NT 4.0 volume sets, stripe sets, and mirror sets can only be managed (deleted, repaired, resynced) with Windows 2000; new equivalents use dynamic volumes.

*Bron: Core Knowledge doc 'Basic and Dynamic disks' (Bas zijn vroege sysadmin-naslag).*

## Verwante notities

- [Basic vs Dynamic Disks](basic-vs-dynamic-disks.md)
- [Partitions and File Systems](partitions-and-filesystems.md)
- [RAID Levels Overview](raid-levels-overview.md)
- [The RAID write penalty](raid-write-penalty.md)
