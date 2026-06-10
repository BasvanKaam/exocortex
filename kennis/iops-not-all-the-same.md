---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [iops, storage, block-size, raid, benchmarking]
layer: rich
bron: inside-citrix-fma
---

# Not all IOPS are the same: the three golden parameters

Bas warns that a random IOPS number on its own means nothing. IOPS can be reads or writes, random or sequential, reread or rewritten, single- or multi-threaded, simultaneous reads and writes, random writes followed by sequential reads of the same data, and span block sizes from bytes to megabytes. Writes are more resource-intensive than reads. Other factors: reading from cache, number of host and disk controllers, storage type, RAID (which negatively impacts the IOPS number due to the write penalty), data tiering, and physical-disk characteristics.

For legacy physical disks, speed and latency depend on RPM (5400, 7200, 10000, 15000 rpm; higher = faster) and disk density (higher density means data is closer together so the read/write head travels less). With a SAN/Filer holding hundreds of disks, 15000 rpm high-density disks make a real difference.

When a vendor claims a crazy-high IOPS number, ask how they tested. At minimum demand the three 'golden' parameters:
- The latency (in ms) involved
- The read vs. write ratio
- The data block sizes used.

Also note that storage throughput (GB/sec bandwidth) is not the same as IOPS, though they overlap.

## Verwante notities

- [In-memory write caching: reducing IOPS needed (PVS RAM Cache with Overflow to Disk)](in-memory-caching-ram-cache-pvs.md)
- [Bas on IOPS, latency and storage sizing](iops-and-latency-fundamentals.md)
- [IOPS fundamentals: latency is king](iops-fundamentals-latency.md)
- [MCS IOPS profile: ~1.6x PVS average, ~1.2x steady state](mcs-iops-vs-pvs.md)
- [Bas's MCS storage implications checklist](mcs-storage-implications.md)
- [Tools and PerfMon counters for measuring IOPS](measuring-iops-tools-and-counters.md)
- [The RAID write penalty](raid-write-penalty.md)
