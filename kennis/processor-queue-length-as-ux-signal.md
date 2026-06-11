---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [vdi, load-testing, performance, pql, cpu, benchmarking]
layer: reference
gedateerd: nee
bron: basvankaam-blog
---

# Processor Queue Length (PQL) as an early UX-degradation signal

A durable performance concept surfaced in the VDI Drones update (Jan 2019): Processor Queue Length (PQL) is a clean indicator of whether a CPU is keeping up. If PQL is zero the CPU is not overwhelmed and user experience is as good as it can be; if the queue builds up, it's an early sign the machine will get slow and UX will suffer. VDI Drones started adding PQL to every chart for exactly this reason. The takeaway generalizes beyond the tool: when load-testing VDI/RDSH, watch queue length, not just raw CPU utilization, as the leading UX indicator.

*Bron: blogpost 'VDI Drones - 2019 update' (2019-01-10), basvankaam.com.*

## Verwante notities

- [Go-EUC: independent community EUC performance research](go-euc-performance-research-platform.md)
- [Good-enough load testing at 10% of the price beats the gold-plated tool](good-enough-load-testing-beats-expensive.md)
- [Linking infrastructure performance to employee productivity](infra-performance-vs-productivity.md)
- [Login VSI and VSImax: benchmarking by saturation](loginvsi-vsimax-saturation-benchmark.md)
- [After disruptive patches, measure impact per workload instead of guessing](measure-dont-guess-capacity-after-patches.md)
- [Meltdown/Spectre patches carried a real performance cost - patch anyway](meltdown-spectre-patch-performance-cost.md)
- [VDI Drones: free Drone client vs paid Controller](vdi-drones-benchmarking-model.md)
- [VDI Drones: synthetic load testing without user accounts (2018)](vdi-drones-synthetic-load-testing.md)
