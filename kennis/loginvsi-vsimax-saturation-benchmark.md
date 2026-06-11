---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [login-vsi, benchmarking, vsimax, vdi, sbc, performance]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Login VSI and VSImax: benchmarking by saturation

How Login VSI worked (2014, v4.0/4.1):

- Unlike conventional steady-state benchmarks (which measure execution time/throughput of fixed processes), Login VSI benchmarks SBC/VDI by saturating the system. It runs simulated user workloads (Office, Internet Explorer, Adobe Reader, etc.) directly inside sessions, gradually adding users until response times escalate.
- The point where response times sharply rise is VSImax (Virtual Session Index), the true maximum active session/desktop capacity. It simplifies comparison and shows the real impact of host- or guest-level config changes.
- Workloads run on the target systems within the session (not via remote sessions); benchmark overhead is small (1-5%).

Version 4.1 changes:
- New 'Office worker' workload; the old Light/Medium/Heavy renamed to Task worker / Knowledge worker / Power worker. Task and Office worker are 1 vCPU; Knowledge and Power worker are 2 vCPU. Office worker sits between Task and Knowledge.
- Can import data from Windows Performance Monitor, VMware ESXtop or any CSV source into the Login VSI Analyzer, with automatic scaling and time synchronisation, to correlate OS/hypervisor/disk metrics.
- VSImax no longer depends specifically on Microsoft Office Word, so you can test without Office; new VSImax measurements help pinpoint CPU vs disk-IO bottlenecks.

Bas calls Login VSI 'the industry standard performance validation solution for centralized virtualized desktop and server-based environments.'

*Bron: blogpost 'LoginVSI advanced performance & scalability testing. What's new with version 4.1?!' (2014-08-03), basvankaam.com.*

## Verwante notities

- [Use-cases for VDI/desktop benchmarking](benchmarking-use-cases.md)
- [Citrix Validated Solution: XenDesktop on Nutanix reference architecture](citrix-validated-solution-nutanix.md)
- [Go-EUC: independent community EUC performance research](go-euc-performance-research-platform.md)
- [Good-enough load testing at 10% of the price beats the gold-plated tool](good-enough-load-testing-beats-expensive.md)
- [Meltdown/Spectre patches carried a real performance cost - patch anyway](meltdown-spectre-patch-performance-cost.md)
- [Processor Queue Length (PQL) as an early UX-degradation signal](processor-queue-length-as-ux-signal.md)
- [Project VRC: a community-sourced SBC/VDI survey](project-vrc-community-survey.md)
- [Project VRC: independent VDI/SBC research and the State of the Union survey](project-vrc-survey-background.md)
- [Benchmarking should not require scripting or fake accounts](stance-no-scripting-benchmarking.md)
- [VDI Drones: free Drone client vs paid Controller](vdi-drones-benchmarking-model.md)
- [VDI Drones: synthetic load testing without user accounts (2018)](vdi-drones-synthetic-load-testing.md)
- [Weighted task mix beats on/off load generation](weighted-randomizer-for-load-task-mix.md)
- [Windows 10 Enterprise multi-session performance debate (Ignite 2019)](wvd-ignite-2019-multisession.md)
