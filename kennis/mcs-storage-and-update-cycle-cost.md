---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, mcs, storage, iops, thin-provisioning, image-management, capacity-planning]
layer: reference
gedateerd: nee
bron: basvankaam-blog
---

# MCS planning: master-VM count x data-store count x update frequency

A durable capacity-planning lesson: each master VM update repeats the full provisioning process. MCS treats an updated master VM as a new master, takes a fresh snapshot, and copies it to every accompanying data store. So the cost scales with: how many distinct master VMs you manage (Win7, Win8, Server 2008R2, 2012R2, etc.), how many data stores you use, and how often each master needs updating. With four master images on a weekly update cycle, that's four snapshots copied to all participating data stores every week, consuming CPU, peaking IO and network. Ask: does your storage support thin provisioning? If not, every provisioned VM is as big as its master. Answering these gives you an indication of storage needs and administrative overhead. Rollbacks are treated the same way, as yet another image differing from the current one.

*Bron: blogpost 'Citrix Machine Creation Services… What to consider!' (2016-02-09), basvankaam.com.*

## Verwante notities

- [The 'big bad image' problem: why everything in the base image hurts](big-bad-base-image-problems.md)
- [MCS desktop types: pooled-random, pooled-static, dedicated](mcs-desktop-types-pooled-dedicated.md)
- [How Citrix MCS provisions VMs: snapshot, differencing disk, identity disk](mcs-how-it-works-disks.md)
- [MCS supported hypervisor storage and thin provisioning limits](mcs-hypervisor-storage-support.md)
- [Why MCS image updates matter: every master VM is re-copied to every datastore](mcs-image-update-repeats-full-copy.md)
- [MCS IOPS profile: ~1.6x PVS average, ~1.2x steady state](mcs-iops-vs-pvs.md)
- [MCS rollbacks and reboot considerations (boot storms, disconnect policies)](mcs-rollbacks-and-reboot-considerations.md)
- [Bas's MCS storage implications checklist](mcs-storage-implications.md)
- [Pooled vs dedicated desktops: the durable trade-off](pooled-vs-dedicated-desktops.md)
- [MCS vs PVS is done to death; pick a lens and stress-test the choice](positie-mcs-not-vs-pvs.md)
- [PVS vs MCS image-delivery tradeoffs (XenDesktop 7 era)](pvs-vs-mcs-tradeoffs.md)
- [Server 2012 R2 data dedup and the VDI separation rule](server-2012-r2-dedup-for-vdi.md)
- [The five VDI workload phases and boot/logon storms](vdi-workload-phases-storms.md)
