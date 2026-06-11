---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [raid, storage, write-penalty, performance]
layer: reference
bron: inside-citrix-fma
---

# The RAID write penalty

RAID configurations bring a write penalty because a parity bit must also be written. A write can't be fully completed until both the data and the parity information are written to disk; the time taken to write the parity bit is the write penalty. This applies only to writes, not reads.

## Verwante notities

- [Dynamic Volume Types](dynamic-volume-types.md)
- [Bas on IOPS, latency and storage sizing](iops-and-latency-fundamentals.md)
- [IOPS fundamentals: latency is king](iops-fundamentals-latency.md)
- [Not all IOPS are the same: the three golden parameters](iops-not-all-the-same.md)
- [MCS supported hypervisor storage and thin provisioning limits](mcs-hypervisor-storage-support.md)
- [Tools and PerfMon counters for measuring IOPS](measuring-iops-tools-and-counters.md)
- [RAM Cache with Overflow to Disk slashes IOPS](ram-cache-overflow-to-disk.md)
