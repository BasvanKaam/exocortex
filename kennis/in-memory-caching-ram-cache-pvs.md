---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [iops, caching, ram, pvs, write-cache]
layer: rich
bron: inside-citrix-fma
---

# In-memory write caching: reducing IOPS needed (PVS RAM Cache with Overflow to Disk)

The storage market offers 'patch'-like solutions (SSD/Flash to speed up legacy SAN/NAS with smart caching) and converged/in-memory caching approaches. Bas highlights that in-memory solutions are special: they don't necessarily increase available IOPS, but decrease the IOPS needed by the workload because writes go to RAM instead of disk, achieving the same or better results.

FMA fact he stresses: by leveraging RAM for writes - Citrix PVS's 'RAM Cache with Overflow to Disk' write cache - you can significantly reduce IOPS needed. Citrix claims to need only 1 to 2 IOPS per user on a XenApp environment without complex configuration or hardware replacement.

Caveat: no matter the accelerator, you must still determine IOPS needed and scale accordingly; even the best IOPS accelerator won't guarantee you can boot the entire VDI infrastructure during daytime without issues. Bas also advises giving your antivirus solution extra attention with VDI.

## Verwante notities

- [Bas on IOPS, latency and storage sizing](iops-and-latency-fundamentals.md)
- [IOPS fundamentals: latency is king](iops-fundamentals-latency.md)
- [Not all IOPS are the same: the three golden parameters](iops-not-all-the-same.md)
- [MCS IOPS profile: ~1.6x PVS average, ~1.2x steady state](mcs-iops-vs-pvs.md)
- [PVS write cache options](pvs-write-cache-options.md)
- [RAM Cache with Overflow to Disk slashes IOPS](ram-cache-overflow-to-disk.md)
- [The five VDI workload phases and boot/logon storms](vdi-five-phases-storms.md)
