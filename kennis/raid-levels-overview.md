---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [storage, raid, reference]
layer: reference
gedateerd: nee
bron: core-knowledge-docs
---

# RAID Levels Overview

Comparison of RAID levels with minimum disks, pros, and cons:

- **JBOD** (min 2): simple to set up; no fault tolerance — a failed disk loses its data.
- **RAID 0** (min 2): fastest throughput, simple; no fault tolerance — one disk failure loses all data.
- **RAID 1** (min 2): full fault tolerance via mirroring, simple, good read performance; relatively expensive.
- **RAID 2** (min 3): error correction even for disks without built-in correction; no practical use.
- **RAID 3** (min 3): fast throughput for contiguous data, efficient error correction; cannot read and write simultaneously.
- **RAID 4** (min 3): good read performance, efficient error correction; slow writes.
- **RAID 5** (min 3): good read performance, efficient error correction, best for network use; write speed depends on the processor/controller doing the parity calculations.
- **RAID 6** (min 4): robust error correction tolerating two failed disks; more compute-intensive than RAID 5, so the controller may cost more.

These level definitions are still accurate today.

*Bron: Core Knowledge doc 'RAID Core Doc' (Bas zijn vroege sysadmin-naslag).*

## Verwante notities

- [Basic vs Dynamic Disks](basic-vs-dynamic-disks.md)
- [Block vs file level storage: the durable trade-off](block-vs-file-level-storage.md)
- [Dynamic Volume Types](dynamic-volume-types.md)
- [Bas on IOPS, latency and storage sizing](iops-and-latency-fundamentals.md)
- [Not all IOPS are the same: the three golden parameters](iops-not-all-the-same.md)
- [NAS vs SAN Storage Architectures](nas-vs-san-storage.md)
