---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [pvs, ram-cache, iops, write-cache, performance]
layer: reference
bron: inside-citrix-fma
---

# RAM Cache with Overflow to Disk slashes IOPS

By leveraging RAM for writes — Citrix PVS's 'RAM Cache with Overflow to Disk' write cache mode — the number of IOPS needed drops significantly. Citrix claims this can bring a XenApp environment down to only 1 to 2 IOPS per user, with no complex configuration or hardware replacement.

## Verwante notities

- [In-memory write caching: reducing IOPS needed (PVS RAM Cache with Overflow to Disk)](in-memory-caching-ram-cache-pvs.md)
- [IOPS fundamentals: latency is king](iops-fundamentals-latency.md)
- [MCS IOPS profile: ~1.6x PVS average, ~1.2x steady state](mcs-iops-vs-pvs.md)
- [PVS write cache options](pvs-write-cache-options.md)
- [The RAID write penalty](raid-write-penalty.md)
- [The five VDI workload phases and boot/logon storms](vdi-five-phases-storms.md)
