---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [iops, perfmon, tool, measurement, login-vsi]
layer: reference
bron: inside-citrix-fma
---

# Tools and PerfMon counters for measuring IOPS

Application vendors often cite Steady State IOPS - the average read/write IOPS over a longer period (a few hours) after machines boot, users log in, and apps launch. To measure your own needs, Performance Monitor (PerfMon) counters help:
- Disk reads/sec - read IOPS
- Disk writes/sec - write IOPS
- Disk transfers/sec - total IOPS
- Current Disk Queue length - IOPS being queued by Windows

Tools to calculate current load or predict needed configuration/IOPS:
1. Iometer - measures IOPS for a workload
2. ESXTOP - ESX-specific disk states, totals, reads/writes
3. WMAROW - web calculator for performance, capacity, random IOPS
4. The Cloud Calculator - disk RAID and IOPS calculator
5. Process Monitor - general IOPS analysis
6. Login VSI - VDI workload generator to simulate user activity

## Verwante notities

- [Bas on IOPS, latency and storage sizing](iops-and-latency-fundamentals.md)
- [IOPS fundamentals: latency is king](iops-fundamentals-latency.md)
- [IOPS, latency, and sizing storage for VDI workloads](iops-latency-and-sizing-storage-for-vdi.md)
- [Not all IOPS are the same: the three golden parameters](iops-not-all-the-same.md)
- [MCS IOPS profile: ~1.6x PVS average, ~1.2x steady state](mcs-iops-vs-pvs.md)
- [The RAID write penalty](raid-write-penalty.md)
- [The five VDI workload phases and boot/logon storms](vdi-five-phases-storms.md)
