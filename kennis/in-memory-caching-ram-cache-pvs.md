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
