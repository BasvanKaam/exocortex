---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [meltdown, spectre, cpu, performance, patching, security]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Meltdown/Spectre patches carried a real performance cost - patch anyway

How it stood in January 2018: Meltdown and Spectre exploited vulnerabilities in modern CPUs (nearly every Intel chip since 1995; Spectre also affects AMD), letting programs steal data being processed (emails, documents, passwords) across laptops, desktops, servers and mobile, on-prem and cloud. Software patches and firmware updates shipped for Windows, Linux, macOS, iOS, Android and Chrome OS.

The catch: the fixes degraded performance and, rushed out, caused reboots and crashes. Early field reports cited CPU utilization up 25-30% and overall performance drops around 20%, varying wildly by CPU model, socket count, and whether the workload hits the kernel. For multi-user (XenApp, RDS, VMware) hosts this means fewer users per host. Bas's emphatic guidance: patch anyway, the security risk is too big. ('Do not let this stop you from patching your machines!')

*Bron: blogpost 'Meltdown and Spectre - Minimize impact and avoid performance problems - how Stratusphere UX can help!' (2018-01-19), basvankaam.com.*

## Verwante notities

- [Login VSI and VSImax: benchmarking by saturation](loginvsi-vsimax-saturation-benchmark.md)
- [After disruptive patches, measure impact per workload instead of guessing](measure-dont-guess-capacity-after-patches.md)
- [Processor Queue Length (PQL) as an early UX-degradation signal](processor-queue-length-as-ux-signal.md)
- [Stratusphere UX is the Swiss Army knife of the portfolio](stratusphere-swiss-army-knife.md)
- [Stratusphere UX 6.1: dashboards, event log harvesting, process optimization](stratusphere-ux-61-features.md)
- [Test quality updates, not just feature updates](test-quality-updates-too.md)
- [VDI Drones: synthetic load testing without user accounts (2018)](vdi-drones-synthetic-load-testing.md)
- [Windows 10 servicing branches and deployment rings](windows10-servicing-branches-rings.md)
