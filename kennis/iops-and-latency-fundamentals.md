---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [iops, latency, storage, sizing, performance]
layer: rich
bron: inside-citrix-fma
---

# Bas on IOPS, latency and storage sizing

Bas's storage philosophy: 'Latency is king' — the less latency, the faster the infrastructure. A high IOPS number is useless unless latency is low; even SSDs that deliver huge IOPS still depend on latency, which tells you how long a single read/write request takes. There is no standard for measuring IOPS — too many factors influence it. A random IOPS number on its own means nothing: you must know reads vs writes, random vs sequential, single/multiple threads, block sizes, and above all the latency in milliseconds. Storage providers should give at least latency (ms), read/write ratio, and block sizes used in testing.

The average/Steady State alone is insufficient — also size for peak activity between boot and Steady State, and distinguish steady state, boot, logon, application-launch and logoff storms. Launching apps generates high read peaks and initial low writes, often causing an unrecognised application launch storm. Storage throughput is not the same as IOPS — throughput (GB/sec) matters for large data volumes. Reads are less intensive than writes and easier to cache. Don't forget CPU, memory and storage controllers as bottlenecks.

Practical fixes: if IOPS are limited, (pre-)boot machines at night and prevent users from rebooting machines themselves.

## Bron-citaten (NL, verbatim)

> Latency is king: the less you have, the faster your infrastructure will be!
>
> A high number of IOPS is useless unless latency is low!

## Verwante notities

- [Bas on CPU over-commit and user baselines (light/medium/heavy)](cpu-overcommit-and-user-baselines.md)
- [In-memory write caching: reducing IOPS needed (PVS RAM Cache with Overflow to Disk)](in-memory-caching-ram-cache-pvs.md)
- [IOPS fundamentals: latency is king](iops-fundamentals-latency.md)
- [Not all IOPS are the same: the three golden parameters](iops-not-all-the-same.md)
- [MCS IOPS profile: ~1.6x PVS average, ~1.2x steady state](mcs-iops-vs-pvs.md)
- [Tools and PerfMon counters for measuring IOPS](measuring-iops-tools-and-counters.md)
- [RAID Levels Overview](raid-levels-overview.md)
- [The RAID write penalty](raid-write-penalty.md)
- [Bas on sizing: there is no 'one size fits all', and don't overdo it](sizing-no-one-size-fits-all.md)
- [The five VDI workload phases and boot/logon storms](vdi-five-phases-storms.md)
