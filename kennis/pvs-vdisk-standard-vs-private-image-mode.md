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
