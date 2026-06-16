---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [moonshot, hdi, hsd, xenapp, virtualization, gpu]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# HP Moonshot: physical one-to-one desktops (HDI) and XenApp cartridges

How it worked then (2015): HP Moonshot delivered Citrix workloads on bare-metal cartridges with no hypervisor, so it was called HDI (Hosted Desktop Infrastructure) rather than VDI. Each user got a physical CPU/GPU on a one-to-one basis. The m700 cartridge held 4 nodes, each a single hosted desktop (AMD Opteron X2150 APU, 1.5 GHz, 4 x86 cores, integrated AMD Radeon HD 8000 GPU, 8 GB DDR3, 32/64 GB iSSD). The m710 cartridge was one XenApp node per cartridge (Intel E3-1284Lv3, integrated Intel Iris Pro P5200 GPU, 32 GB RAM, 120/480 GB M.2 SSD) and could also host other application-delivery or video-transcoding workloads. A full chassis held 45 cartridges, so up to 45 XenApp servers or 45 x 4 = 180 hosted desktops. Benefits were predictability, linear scaling, no boot storms, and excellent isolated UX. Drawbacks: all-physical (still needs a separate platform for AD/DNS/StoreFront/controllers), no MCS/PVS-free management gains, cartridges sold ~15 at a time, and unused cartridge compute could not be repurposed.

*Bron: blogpost 'HP Moonshot revisited. Well... by me anyway' (2015-06-30), basvankaam.com.*

## Verwante notities

- [HP Moonshot is converged but not truly web-scale](hp-moonshot-is-not-web-scale.md)
- [Intel entering vGPU turns the GPU space into a three-way race](intel-enters-vgpu-three-way-race.md)
- [Delivering a desktop OS multi-tenant via dedicated Moonshot cartridges](moonshot-desktop-os-multi-tenancy-licensing.md)
- [HP Moonshot as HDI: physical desktops, no hypervisor layer](moonshot-hdi-physical-no-hypervisor.md)
- [Bas: companies are swinging back from virtual/cloud to physical](swing-back-from-virtual-to-physical-2018.md)
- [Virtual usually beats physical, but leasing changes the Moonshot math](virtual-beats-physical-but-leasing-changes-moonshot-math.md)
