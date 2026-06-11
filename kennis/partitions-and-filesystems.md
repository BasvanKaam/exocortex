---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [storage, partitions, ntfs, fat, windows]
layer: reference
gedateerd: nee
bron: core-knowledge-docs
---

# Partitions and File Systems

A partition is a section of a physical disk that behaves as if it were a separate physical disk, and it must be formatted independently (FAT, FAT32, or NTFS). Partitions only exist on **basic disks**.

Partition roles:

- **System partition**: holds the files needed to load the OS (e.g. the boot loader, boot configuration). 
- **Boot partition**: holds the OS itself and its support files. It can be the same partition as the system partition, but need not be.
- **Active partition**: the partition the computer boots from; must be a primary partition on a basic disk.
- **Primary partition**: a volume on free space of a basic disk. Up to 4 primaries, or 3 primaries plus 1 extended; primaries cannot be subdivided.
- **Extended partition**: a region of a basic disk that can contain logical drives. Use it when you need more than 4 volumes; no primary is required to create one.
- **Logical drive**: a volume created inside an extended partition, which can be formatted and assigned a drive letter.

*Bron: Core Knowledge doc 'Basic and Dynamic disks' (Bas zijn vroege sysadmin-naslag).*

## Verwante notities

- [Basic vs Dynamic Disks](basic-vs-dynamic-disks.md)
- [Dynamic Volume Types](dynamic-volume-types.md)
- [Disk Fragmentation: FAT vs NTFS](fragmentation-fat-vs-ntfs.md)
- [Share vs NTFS Permissions](share-vs-ntfs-permissions.md)
