---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [mcs, differencing-disk, identity-disk, write-cache, active-directory]
layer: reference
bron: inside-citrix-fma
---

# MCS Differencing Disk and Identity Disk

Every VM created by MCS consists of two disks attached to it (the exact technical handling differs slightly per hypervisor):

- **Differencing Disk**: stores all changes made to the VM; it functions as a write cache.
- **Identity Disk**: gives the VM its own identity used within Active Directory.

During provisioning, MCS first takes a snapshot of the master VM (automatically, or you can take one manually so you can name it yourself). The snapshot is consolidated (merged) and a temporary VM is created and booted so that tasks like DHCP and KMS can be handled, before being copied over to all datastores in the deployment. MCS also takes care of machine account creation in Active Directory during this phase.

## Verwante notities

- [Machine Creation Services essentials](machine-creation-services-essentials.md)
- [Machine Creation Services (MCS): integrated single-image delivery](machine-creation-services-overview.md)
- [MCS desktop types: Pooled-Random, Pooled-Static, Dedicated](mcs-desktop-types.md)
- [Why MCS image updates matter: every master VM is re-copied to every datastore](mcs-image-update-repeats-full-copy.md)
- [MCS IOPS profile: ~1.6x PVS average, ~1.2x steady state](mcs-iops-vs-pvs.md)
- [MCS updating: persistent vs non-persistent VM behaviour](mcs-updating-persistent-vs-nonpersistent.md)
- [Personal vDisks (PvD)](pvs-personal-vdisks-pvd.md)
- [PVS vDisk creation, Standard vs Private Image Mode](pvs-vdisk-standard-vs-private-image-mode.md)
