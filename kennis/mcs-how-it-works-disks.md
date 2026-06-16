---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, mcs, differencing-disk, identity-disk, master-vm, golden-image, host-connection]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# How Citrix MCS provisions VMs: snapshot, differencing disk, identity disk

How it worked then: MCS is built right into XenDesktop/XenApp (no separate infrastructure to build and maintain, unlike PVS). It starts from a master VM (golden image). When you create a Machine Catalog in Studio, MCS takes a snapshot of the master (or you take one manually, with the advantage of naming it), then copies that template to all data stores known to the Host Connection. Each provisioned VM consists of a differencing disk (stores all changes, acts as write cache) and an identity disk (gives the VM its own identity, e.g. for Active Directory); how this attaches differs per hypervisor. As of XenDesktop 7.0, MCS can also provision Server OS machines. MCS cannot provision physical machines (PVS can). MCS can assign persistent VMs using Personal vDisks (PvD), though that's a cumbersome, unpopular approach.

*Bron: blogpost 'Citrix Machine Creation Services… What to consider!' (2016-02-09), basvankaam.com.*

## Verwante notities

- [Citrix Host Connection](citrix-host-connection.md)
- [Copy-on-Write Snapshots vs Clones](copy-on-write-snapshots-vs-clones.md)
- [Machine Creation Services (MCS): integrated single-image delivery](machine-creation-services-overview.md)
- [MCS desktop types: pooled-random, pooled-static, dedicated](mcs-desktop-types-pooled-dedicated.md)
- [MCS Differencing Disk and Identity Disk](mcs-differencing-and-identity-disk.md)
- [Why MCS image updates matter: every master VM is re-copied to every datastore](mcs-image-update-repeats-full-copy.md)
- [MCS planning: master-VM count x data-store count x update frequency](mcs-storage-and-update-cycle-cost.md)
- [Personal vDisk: persistence of dedicated, manageability of pooled](personal-vdisk-pvd-concept.md)
- [Pooled vs dedicated desktops: the durable trade-off](pooled-vs-dedicated-desktops.md)
- [MCS vs PVS is done to death; pick a lens and stress-test the choice](positie-mcs-not-vs-pvs.md)
- [PVS vs MCS image-delivery tradeoffs (XenDesktop 7 era)](pvs-vs-mcs-tradeoffs.md)
- [VM Snapshot Mechanics: Delta Files and Redo Logs](vm-snapshot-delta-mechanics.md)
- [How VMware Instant Clones (vmFork) provision desktops in seconds](vmware-instant-clones-vmfork-mechanics.md)
- [XenDesktop 7 Host Infrastructure and what it unlocks](xendesktop-host-infrastructure-mcs-pvs.md)
