---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [vdi, iops, boot-storm, logon-storm, steady-state]
layer: rich
bron: inside-citrix-fma
---

# The five VDI workload phases and boot/logon storms

Bas breaks a VDI workload into five phases: boot, user logon, application launch, Steady State, and logoff/shutdown.

- Boot: creates a huge spike in read I/O. Booting many VMs at once creates a 'boot storm' that can hurt performance. FMA fact: if IOPS are limited, (pre-)boot machines at night and prevent users from rebooting themselves - though daytime reboots may still be unavoidable.
- Logon: always happens during the day (can't be scheduled at night). Generates high reads (less than boot) and nearly equal writes, due to software starting at logon and how user profiles load. Application virtualisation, layering, folder redirection, and Flex Profiles greatly enhance performance.
- Application launch: high read I/O peaks and initial low writes, causing an often-unrecognised 'application launch storm'.
- Steady State: write I/O takes over from read I/O, averaging roughly the 20:80 read/write ratio (a figure heard in MCS vs PVS discussions). Average IOPS alone isn't sufficient - you must also size for the peaks between boot and Steady State.
- Logoff/shutdown: a large write peak with very little read activity; plan for write peaks here just as for read peaks at boot/logon.

Reads are less demanding than writes and can be cached (read from memory on repeat requests), but caching won't solve everything - you still must calculate and size. Don't assume the disk subsystem is the only bottleneck: storage controllers, CPU, memory, network, RAID penalties, and compression/de-duplication can all be limiters.

## Verwante notities

- [Bas on CPU over-commit and user baselines (light/medium/heavy)](cpu-overcommit-and-user-baselines.md)
- [FlexCast delivery technology, worker types and delivery models](flexcast-delivery-models-and-worker-types.md)
- [In-memory write caching: reducing IOPS needed (PVS RAM Cache with Overflow to Disk)](in-memory-caching-ram-cache-pvs.md)
- [Bas on IOPS, latency and storage sizing](iops-and-latency-fundamentals.md)
- [IOPS fundamentals: latency is king](iops-fundamentals-latency.md)
- [MCS IOPS profile: ~1.6x PVS average, ~1.2x steady state](mcs-iops-vs-pvs.md)
- [MCS rollbacks and reboot considerations (boot storms, disconnect policies)](mcs-rollbacks-and-reboot-considerations.md)
- [Bas's MCS storage implications checklist](mcs-storage-implications.md)
- [Tools and PerfMon counters for measuring IOPS](measuring-iops-tools-and-counters.md)
- [RAM Cache with Overflow to Disk slashes IOPS](ram-cache-overflow-to-disk.md)
- [Bas on sizing: there is no 'one size fits all', and don't overdo it](sizing-no-one-size-fits-all.md)
