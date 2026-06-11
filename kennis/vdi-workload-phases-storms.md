---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [vdi, iops, boot-storm, logon-storm, steady-state, pvs, ram-cache]
layer: reference
gedateerd: nee
bron: basvankaam-blog
---

# The five VDI workload phases and boot/logon storms

Durable VDI sizing model (2014, still conceptually valid):

A VDI workload breaks into five phases: boot, user logon, application launch, Steady State, and logoff/shutdown.

- Boot: huge read I/O spike. Many VMs booting at once = a boot storm. Mitigate by pre-booting at night and preventing users from rebooting themselves; but daytime reboots may still be unavoidable.
- Logon: high reads (less than boot) and near-equal writes, driven by startup software and profile loading. A logon storm always happens in the morning and can't be scheduled away. App streaming, folder redirection and flex profiles help.
- App launch: high read peaks, low initial writes (an often-unrecognised 'application launch storm').
- Steady State: write I/O takes over, roughly a 20/80 read/write ratio. This is the average over hours. Average alone isn't enough; you must also size for the read/write peaks.
- Logoff/shutdown: large write peak, little read.

Key point: scale for the peaks (read and write), not just the Steady State average. Perfmon counters to watch: Disk reads/sec, Disk writes/sec, Disk transfers/sec (total IOPS), Current Disk Queue Length (IOPS being queued by Windows).

RAM-cache solutions (e.g. Citrix PVS RAM Cache with Overflow to Disk) don't add IOPS; they reduce IOPS needed by sending writes to RAM instead of disk. Citrix claimed only 1-2 IOPS per user on XenApp with this approach.

*Bron: blogpost 'The ultimate IOPS cheat sheet!' (2014-07-29), basvankaam.com.*

## Verwante notities

- [Block vs file level storage, plainly](block-vs-file-storage.md)
- [When someone quotes an IOPS number, ask which block size](iops-always-ask-block-size.md)
- [IOPS fundamentals: latency is king](iops-latency-fundamentals.md)
- [Be skeptical of any vendor's headline IOPS number](iops-marketing-skepticism.md)
- [MCS planning: master-VM count x data-store count x update frequency](mcs-storage-and-update-cycle-cost.md)
- [Pooled vs dedicated desktops: the durable trade-off](pooled-vs-dedicated-desktops.md)
- [Killing VDI IOPS with PVS write cache in RAM](pvs-write-cache-in-ram.md)
- [VDI is more romantic on paper than in reality](vdi-romantic-vs-reality-position.md)
