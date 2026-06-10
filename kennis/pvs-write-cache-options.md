---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [citrix, pvs, write-cache, ram, performance]
layer: reference
bron: inside-citrix-fma
---

# PVS write cache options

A read-only Standard Image vDisk can't store the writes a booting/running machine produces, so each target device gets its own **write cache**. In Standard Image mode the write cache is cleared on reboot (a fresh start); in Private Image mode changes persist. Options:

- **Cache on device hard drive:** stored on the target's local (virtual/physical) disk; no extra software, configured in the PVS console; refreshed on reboot. Recommended when RAM caching isn't possible.
- **Cache on device hard drive persisted:** same, but changes survive reboot; needs a different bootstrap file.
- **Cache on a server:** writes handled on the provisioning server, increasing disk IO and network bandwidth; Bas does not recommend this.
- **Cache on server persistent:** each device gets its own writable, persistent file on the server; changes survive reboot.
- **Cache in device RAM:** writes stored temporarily in the target's RAM — by far the fastest method.
- **Cache in device RAM with overflow on HDD:** writes go to RAM first; when RAM fills, least-recently-used blocks spill to local disk (VHDX differencing format). The RAM used is non-paged kernel memory. More RAM = better experience. Together with plain 'cache in device RAM', this is the preferred way to implement PVS write cache.

Bas's view on persistent desktops via PVS or MCS (PvD): not a common approach — he'd recommend full VMs instead.

## Verwante notities

- [In-memory write caching: reducing IOPS needed (PVS RAM Cache with Overflow to Disk)](in-memory-caching-ram-cache-pvs.md)
- [IOPS fundamentals: latency is king](iops-fundamentals-latency.md)
- [Provisioning Services essentials and Bas's advice](provisioning-services-essentials.md)
- [Bas's PVS key takeaways and best-practice asides](provisioning-services-key-takeaways.md)
- [Citrix Provisioning Services (PVS) overview](provisioning-services-overview.md)
- [PVS high availability](pvs-high-availability.md)
- [Personal vDisks (PvD)](pvs-personal-vdisks-pvd.md)
- [PVS vDisk creation, Standard vs Private Image Mode](pvs-vdisk-standard-vs-private-image-mode.md)
- [PVS vDisk versioning and lifecycle](pvs-vdisk-versioning-lifecycle.md)
- [RAM Cache with Overflow to Disk slashes IOPS](ram-cache-overflow-to-disk.md)
