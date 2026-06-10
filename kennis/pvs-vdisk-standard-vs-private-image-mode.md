---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [citrix, pvs, vdisk, master-target-device, write-cache]
layer: reference
bron: inside-citrix-fma
---

# PVS vDisk creation, Standard vs Private Image Mode

A vDisk starts on a **Master Target Device** — a physical or virtual machine where you install all desired software (often using SCCM or similar) like a master image. Using PVS client software installed on it, a vDisk is exported from the device's local hard drive. vDisks can be stored locally on the provisioning server, on a network share, or on shared storage accessible by all provisioning servers; storage choice matters because hundreds of machines may hit the same vDisk (though most reads come from cache after the first machines boot).

Two assignment modes:
- **Standard Image Mode** (read-only): the vDisk is shared by multiple devices simultaneously. Each machine has its own **Write Cache** for writes to the read-only vDisk.
- **Private Image Mode** (one-to-one): the user can read and write to the vDisk, and all changes are saved persistently.

## Verwante notities

- [Bas's PVS recommendation: hybrid versioning approach](bas-pvs-hybrid-versioning-recommendation.md)
- [MCS Differencing Disk and Identity Disk](mcs-differencing-and-identity-disk.md)
- [Citrix Provisioning Services (PVS) overview](provisioning-services-overview.md)
- [PVS boot mechanism: Bootstrap, TFTP and BDM](pvs-boot-mechanism-bootstrap-tftp-bdm.md)
- [PVS high availability](pvs-high-availability.md)
- [Personal vDisks (PvD)](pvs-personal-vdisks-pvd.md)
- [PVS provisioning wizards: streamed VM and XenDesktop setup](pvs-provisioning-wizards.md)
- [PVS terminology: Farm, Site, Store, Device Collection, Target Device](pvs-terminology-farm-site-store-collection.md)
- [PVS vDisk versioning and lifecycle](pvs-vdisk-versioning-lifecycle.md)
- [PVS write cache options](pvs-write-cache-options.md)
