---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [storage, defragmentation, ntfs, fat, performance]
layer: reference
gedateerd: ja
bron: core-knowledge-docs
---

# Disk Fragmentation: FAT vs NTFS

Fragmentation is the scattering of one file's pieces across different regions of a disk, which slows disk access and overall performance.

- **FAT** partitions use a File Allocation Table, smaller than NTFS's Master File Table (MFT). On equally sized disks, a FAT partition has a larger cluster size than NTFS.
- **NTFS** partitions have a larger MFT, and Windows never fills the very start of the disk during defrag because that area is reserved for the MFT. NTFS's smaller cluster size means such a disk can be defragmented less far than a FAT one.

Bas's observed lab figures (member server, C:): 17% total / 34% file fragmentation; on a DC: 22% total / 45% file fragmentation - the kind of before/after baseline he recorded when defragging. Note: tools like Diskeeper offered scheduled ("Set It and Forget It") and boot-time defragmentation, including network-wide scheduling in the server version.

*Bron: Core Knowledge doc 'Basic and Dynamic disks' (Bas zijn vroege sysadmin-naslag).*

## Verwante notities

- [Basic vs Dynamic Disks](basic-vs-dynamic-disks.md)
- [Partitions and File Systems](partitions-and-filesystems.md)
- [Share vs NTFS Permissions](share-vs-ntfs-permissions.md)
