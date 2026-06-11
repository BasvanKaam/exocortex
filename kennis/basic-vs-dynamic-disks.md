---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [storage, dynamic-disks, disk-management, windows-2000]
layer: reference
gedateerd: ja
bron: core-knowledge-docs
---

# Basic vs Dynamic Disks

Reference on the Windows 2000-era disk model:

- **Basic disk**: a physical disk holding primary/extended partitions and logical drives. Can host RAID. Uses partitions to divide capacity.
- **Dynamic disk**: a physical disk managed by Disk Management. Holds only dynamic **volumes**, not partitions or logical drives, and cannot be accessed from MS-DOS. Capacity is divided across volumes rather than partitions.

You can upgrade basic to dynamic, and existing partitions convert to volumes. An active partition on a basic disk, once upgraded, becomes an active simple volume (the active/boot volume must be a simple volume on a dynamic disk). The conversion is one-directional in practice.

*Bron: Core Knowledge doc 'Basic and Dynamic disks' (Bas zijn vroege sysadmin-naslag).*

## Verwante notities

- [Dynamic Volume Types](dynamic-volume-types.md)
- [Disk Fragmentation: FAT vs NTFS](fragmentation-fat-vs-ntfs.md)
- [Partitions and File Systems](partitions-and-filesystems.md)
- [RAID Levels Overview](raid-levels-overview.md)
