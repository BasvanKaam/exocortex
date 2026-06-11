---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, mcs, vdi, provisioning, xendesktop]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# MCS desktop types: pooled-random, pooled-static, dedicated

How it worked then: Machine Creation Services (MCS) provisioned client-OS desktops from a single base (master/golden) image. Each provisioned VM got an identity disk (16 MB, for AD identity) and a differencing disk for all writes, linked to a read-only full clone of a snapshot of the master placed in the storage repository.

The three classic machine types:
- Pooled-Random: desktops assigned randomly; on reboot all changes are deleted and the desktop returns to the pool.
- Pooled-Static: desktop permanently assigned to one user, but changes are still destroyed on reboot.
- Dedicated: permanently assigned and changes persist across reboots.

The core trade-off: pooled keeps management easy and storage low but users lose personalisation; dedicated keeps users happy but storage grows (differencing disks keep expanding) and each desktop drifts unique, raising management cost. A dedicated desktop's differencing disk also could not have its underlying base image updated from Studio without destroying it. Durable lesson under the dated UI: stateless pooled vs persistent dedicated is the fundamental VDI image trade-off.

*Bron: blogpost 'XenDesktop (MCS) Personal vDisks' (2013-09-22), basvankaam.com.*

## Verwante notities

- [Instant Clones are for non-persistent floating VDI only](instant-clones-use-case-and-limits.md)
- [MCS desktop types: Pooled-Random, Pooled-Static, Dedicated](mcs-desktop-types.md)
- [MCS Differencing Disk and Identity Disk](mcs-differencing-and-identity-disk.md)
- [How Citrix MCS provisions VMs: snapshot, differencing disk, identity disk](mcs-how-it-works-disks.md)
- [MCS planning: master-VM count x data-store count x update frequency](mcs-storage-and-update-cycle-cost.md)
- [Bas's MCS storage implications checklist](mcs-storage-implications.md)
- [MCS updating: persistent vs non-persistent VM behaviour](mcs-updating-persistent-vs-nonpersistent.md)
- [Personal vDisk: persistence of dedicated, manageability of pooled](personal-vdisk-pvd-concept.md)
- [Pooled vs dedicated desktops: the durable trade-off](pooled-vs-dedicated-desktops.md)
- [Positie: Personal vDisk is great and underappreciated](positie-pvd-underappreciated.md)
- [PVS vs MCS image-delivery tradeoffs (XenDesktop 7 era)](pvs-vs-mcs-tradeoffs.md)
- [VDI is more romantic on paper than in reality](vdi-romantic-vs-reality-position.md)
- [How VMware Instant Clones (vmFork) provision desktops in seconds](vmware-instant-clones-vmfork-mechanics.md)
