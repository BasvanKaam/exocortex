---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [load-testing, benchmarking, vdi-drones, gourami, login-vsi, capacity-planning]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# VDI Drones: synthetic load testing without user accounts (2018)

How it worked at launch. VDI Drones (Gourami software, by Dennis Smith) generates synthetic load to size and stress-test VDI, Hosted Shared (RDSH) or DaaS infrastructure across all major hypervisors (VMware, Hyper-V, XenServer, Nutanix Acropolis) and clouds (Azure, AWS). It is a portable Windows .exe (.NET 4.0+), no install and no scripting needed.

Architecture: two components. The Drone runs on each target VM and generates the actual load; the Controller (a domain-joined machine) deploys/starts/stops Drones, gathers live performance data, and lets you configure load profiles. A load profile (.cfg) specifies threads, in-between idle times, CPU in-use %, memory claim, memory copy, file read and file write, each with min/max ranges, executed in random sequence. The same profile is applied to all selected machines (picked from Active Directory). "Performance watchers" are key machines (PVS servers, Delivery Controllers, file/domain controllers) configured to emit an HTML performance report every 15 minutes; one Controller was verified handling up to 20 watchers across a 10,000-machine test.

Key design choice: it does NOT create or log in users, open apps, or measure user experience. The rationale: every login is ultimately just a claim on CPU/memory/IO/network, creating thousands of test accounts is often politically or practically infeasible, and no synthetic tool can truly replicate real user behavior anyway. Requires admin rights on Controller and Drones, access to RPC$ and WMI queries, and Windows remoting allowed. Use cases: validate a new build under load, measure impact of changes/patches (Meltdown/Spectre cited), burn-in testing of new hardware.

*Bron: blogpost 'Introducing VDI Drones load testing tool' (2018-09-04), basvankaam.com.*

## Verwante notities

- [Use-cases for VDI/desktop benchmarking](benchmarking-use-cases.md)
- [Go-EUC: independent community EUC performance research](go-euc-performance-research-platform.md)
- [Good-enough load testing at 10% of the price beats the gold-plated tool](good-enough-load-testing-beats-expensive.md)
- [Login VSI and VSImax: benchmarking by saturation](loginvsi-vsimax-saturation-benchmark.md)
- [After disruptive patches, measure impact per workload instead of guessing](measure-dont-guess-capacity-after-patches.md)
- [Meltdown/Spectre patches carried a real performance cost - patch anyway](meltdown-spectre-patch-performance-cost.md)
- [Processor Queue Length (PQL) as an early UX-degradation signal](processor-queue-length-as-ux-signal.md)
- [Ship sensible defaults, because people don't read the manual](ship-defaults-because-people-dont-read-manuals.md)
- [VDI Drones: free Drone client vs paid Controller](vdi-drones-benchmarking-model.md)
- [Weighted task mix beats on/off load generation](weighted-randomizer-for-load-task-mix.md)
