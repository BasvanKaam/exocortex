---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [vdi-drones, benchmarking, load-testing, vdi, wvd]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# VDI Drones: free Drone client vs paid Controller

How it worked then (2021, v3.2): VDI Drones is benchmarking/load-testing software for corporate environments, able to benchmark from 1 up to ~10,000 machines with a few clicks and no scripting. First released in 2015.

Licensing/architecture:
- The **Drone** (client doing the test) is free and portable: a single `.exe`, no install or registration. Benchmarks or stress-tests one physical or virtual machine; the only ask is that you agree to share your scores. Compatible with Microsoft Windows Virtual Desktop, so you can verify the IOPS an Azure VM actually delivers.
- The **Controller** is the paid part and requires the Drone. It fetches a machine list from Active Directory and benchmarks/load-tests hundreds of machines at once; a limited free trial is available.

v3.2 additions: WPF GUI rebuild; CPU sub-tests (ALU, FPU, encryption, compression), multi-core benchmark by default, L1 cache test; memory latency test; extensive IO test (4k, 4k-64, sequential, access time, reads and writes); predefined load profiles (Light, Normal, High, Insane) plus custom load/save.

Key new Controller feature **Autotune**: apply a slowly increasing load while watching Processor Queue Length to determine how many machines an environment can host while remaining workable. The pitch (per Dennis): no PowerShell and no creating hundreds of user accounts needed, just the software and proper permissions.

*Bron: blogpost 'VDI Drones 3.2 has been released. Find out what's new' (2021-03-19), basvankaam.com.*

## Verwante notities

- [Use-cases for VDI/desktop benchmarking](benchmarking-use-cases.md)
- [Go-EUC: independent community EUC performance research](go-euc-performance-research-platform.md)
- [Good-enough load testing at 10% of the price beats the gold-plated tool](good-enough-load-testing-beats-expensive.md)
- [Linking infrastructure performance to employee productivity](infra-performance-vs-productivity.md)
- [Login VSI and VSImax: benchmarking by saturation](loginvsi-vsimax-saturation-benchmark.md)
- [Processor Queue Length (PQL) as an early UX-degradation signal](processor-queue-length-as-ux-signal.md)
- [Ship sensible defaults, because people don't read the manual](ship-defaults-because-people-dont-read-manuals.md)
- [Benchmarking should not require scripting or fake accounts](stance-no-scripting-benchmarking.md)
- [VDI Drones: synthetic load testing without user accounts (2018)](vdi-drones-synthetic-load-testing.md)
- [Weighted task mix beats on/off load generation](weighted-randomizer-for-load-task-mix.md)
