---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [iops, latency, storage, vdi, avd, sizing, performance]
layer: reference
gedateerd: nee
bron: nerdio-blog
---

# IOPS, latency, and sizing storage for VDI workloads

Bas's plain-language explainer on storage performance for desktop workloads. Durable fundamentals, not version-specific.

## IOPS vs latency (the key distinction)
- IOPS = input/output operations per second, a read or a write. A disk capable of 100 IOPS can theoretically issue 100 read/write operations per second.
- But issuing is not the same as processing. **Latency** tells you how long each operation actually takes.
- Worked example: a subsystem that can issue 100 IOPS but processes each at 20 ms only handles 50 IOPS in practice. 1 second = 1000 ms; 1000 ms / 20 ms = 50 IOPS. Latency makes all the difference.
- A raw IOPS number on its own says little.

## Acceptable response times (rule of thumb, in ms)
- 0-12 ms: fine; lower is better.
- 10-15 ms: acceptable in most cases; user may notice a small delay.
- 15-20 ms: users experience slow responsiveness.
- 20-25 ms: not good, action needed.

## Why IOPS is hard to measure
Many IOPS types exist. Cache reads are much faster than disk; reads are faster and less resource-intensive than writes. Block sizes vary (many small blocks take longer than a few large ones); I/O can be sequential or random; there are re-reads and re-writes, single and multi-threaded, all mixed. There is no single standard way to measure IOPS; each workload has its own characteristics.

## Steady state vs peak
- **Steady state**: the average reads/writes processed over a longer period (hours) once users are logged in and working. Good baseline for whether users will be happy.
- The steady-state sweet spot is roughly **20/80 reads/writes** (mostly writes). Your mileage varies, and single-user vs multi-user changes the picture. Rule of thumb.
- **Peak** matters too: boot, logon and launch storms spike far above steady state. Size for peaks, not just averages.

*Bron: Nerdio-content 'Ephemeral OS Disks' (Blogs).*

## Verwante notities

- [Azure Ephemeral OS Disks (and Why They Fit Stateless AVD/WVD)](azure-ephemeral-os-disks-explainer.md)
- [Azure Files tiers and pricing model (reference)](azure-files-tiers-reference.md)
- [Ephemeral OS Disks for AVD: free, fast OS storage for stateless hosts](ephemeral-os-disks-for-avd.md)
- [Bas on IOPS, latency and storage sizing](iops-and-latency-fundamentals.md)
- [Not all IOPS are the same: the three golden parameters](iops-not-all-the-same.md)
- [Latency is king, not raw IOPS](latency-is-king-iops-context.md)
- [Tools and PerfMon counters for measuring IOPS](measuring-iops-tools-and-counters.md)
- [Nerdio Manager storage autoscale for Azure Files Premium](nerdio-azure-files-premium-autoscale.md)
- [The five VDI workload phases and boot/logon storms](vdi-five-phases-storms.md)
- [Size virtual desktops by testing, not by general guidelines](wvd-sizing-test-dont-trust-guidelines.md)
