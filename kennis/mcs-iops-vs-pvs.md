---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [mcs, iops, storage, steady-state, read-cache]
layer: reference
bron: inside-citrix-fma
---

# MCS IOPS profile: ~1.6x PVS average, ~1.2x steady state

MCS can be storage-intensive on read IOPS. On average it needs around 1.6x more IOPS than PVS (mainly read traffic from the master VM). But that 1.6 number is the overall average, which includes boot and logon storms (why it is mostly read IOPS). If you focus on steady-state IOPS only, it is closer to 1.2x: a big difference.

Workload examples (per user):
- A medium workload (Login VSI medium) on a Windows 7/8 VM provisioned with MCS needs ~12 IOPS at steady state with a 20:80 read/write ratio. During boot this flips to ~80:20.
- The same workload on a Server 2012 R2 VM needs ~9 IOPS at steady state, 20:80 read/write, again ~80:20 during boot.

Reads cache very well: don't be surprised to hit a read cache ratio of 75% or higher, boosting performance. Citrix IOPS best-practice recommendations are almost exclusively based on steady-state operations.

## Verwante notities

- [In-memory write caching: reducing IOPS needed (PVS RAM Cache with Overflow to Disk)](in-memory-caching-ram-cache-pvs.md)
- [Bas on IOPS, latency and storage sizing](iops-and-latency-fundamentals.md)
- [Not all IOPS are the same: the three golden parameters](iops-not-all-the-same.md)
- [MCS Differencing Disk and Identity Disk](mcs-differencing-and-identity-disk.md)
- [MCS supported hypervisor storage and thin provisioning limits](mcs-hypervisor-storage-support.md)
- [Why MCS image updates matter: every master VM is re-copied to every datastore](mcs-image-update-repeats-full-copy.md)
- [Bas's MCS storage implications checklist](mcs-storage-implications.md)
- [Tools and PerfMon counters for measuring IOPS](measuring-iops-tools-and-counters.md)
- [RAM Cache with Overflow to Disk slashes IOPS](ram-cache-overflow-to-disk.md)
- [Bas on sizing: there is no 'one size fits all', and don't overdo it](sizing-no-one-size-fits-all.md)
- [The five VDI workload phases and boot/logon storms](vdi-five-phases-storms.md)
