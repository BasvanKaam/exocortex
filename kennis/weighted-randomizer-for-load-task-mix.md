---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [vdi, load-testing, benchmarking, vdi-drones, tuning]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Weighted task mix beats on/off load generation

A design improvement in VDI Drones (2019): instead of toggling CPU and Disk load tasks simply on/off (0 or 1), you assign a weight (e.g. 66 to CPU, 34 to Disk) and a weighted randomizer picks tasks accordingly. This lets you fine-tune the synthetic load profile to better match a real workload mix. The general principle for benchmarking tools: weighting the task distribution gives more realistic and efficient load shaping than binary enable/disable.

*Bron: blogpost 'VDI Drones - 2019 update' (2019-01-10), basvankaam.com.*

## Verwante notities

- [Use-cases for VDI/desktop benchmarking](benchmarking-use-cases.md)
- [Good-enough load testing at 10% of the price beats the gold-plated tool](good-enough-load-testing-beats-expensive.md)
- [Login VSI and VSImax: benchmarking by saturation](loginvsi-vsimax-saturation-benchmark.md)
- [Ship sensible defaults, because people don't read the manual](ship-defaults-because-people-dont-read-manuals.md)
- [Benchmarking should not require scripting or fake accounts](stance-no-scripting-benchmarking.md)
- [VDI Drones: free Drone client vs paid Controller](vdi-drones-benchmarking-model.md)
- [VDI Drones: synthetic load testing without user accounts (2018)](vdi-drones-synthetic-load-testing.md)
