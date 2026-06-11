---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [sizing, capacity-planning, testing, methodology]
layer: rich
bron: inside-citrix-fma
---

# Bas on sizing: there is no 'one size fits all', and don't overdo it

For XenApp, sizing is about how many users you can fit on a single (physical or virtual) machine without compromising the user experience; for XenDesktop VDI it is always one user per desktop, ideally performing as close to (or better than) a physical PC. Bas stresses there is no 'one size fits all', because it depends on application types (video, audio, number crunching), usage intensity, and the OS used.

The underlying storage infrastructure plays an important role: all the CPU/GPU/memory in the world won't help if storage can't deliver the required IOPS and throughput. Machine type (persistent vs non-persistent) and provisioning mechanism (MCS vs PVS, with their differing write-cache and differencing-disk impacts) also matter.

His key warning: don't overdo the calculations. Even weeks of storage/compute calculation and load testing guarantee nothing because users are unpredictable; these are only indications. Real-world testing is the only true way to validate what you have built - see what happens and talk to your users.

## Bron-citaten (NL, verbatim)

> Real-world testing, as highlighted earlier, is the only true way of validating what you have built. See what happens and talk to your users.

## Verwante notities

- [Citrix Project Accelerator: web-based design guidance](citrix-project-accelerator.md)
- [Bas on CPU over-commit and user baselines (light/medium/heavy)](cpu-overcommit-and-user-baselines.md)
- [Firm believer in choice: spread options, but cap the platform count](firm-believer-in-choice-no-one-size-fits-all.md)
- [Bas on IOPS, latency and storage sizing](iops-and-latency-fundamentals.md)
- [MCS IOPS profile: ~1.6x PVS average, ~1.2x steady state](mcs-iops-vs-pvs.md)
- [After disruptive patches, measure impact per workload instead of guessing](measure-dont-guess-capacity-after-patches.md)
- [Sizing resources: XenDesktop Design Handbook and community calculators](sizing-resources-and-handbook.md)
- [StoreFront server sizing and supported OSes](storefront-server-sizing.md)
- [Bas's troubleshooting and sizing philosophy](troubleshooting-and-sizing-philosophy.md)
- [The five VDI workload phases and boot/logon storms](vdi-five-phases-storms.md)
