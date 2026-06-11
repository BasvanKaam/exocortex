---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [vmware, instant-clones, vmfork, vdi, horizon, copy-on-write]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# How VMware Instant Clones (vmFork) provision desktops in seconds

Instant Clones, a.k.a. Just-In-Time (JIT) desktops or vmFork, clone a running VM in roughly a second via in-memory cloning of a parent VM plus copy-on-write. The chain, as it worked in Horizon 7 Enterprise: you pick a snapshot of the master VM; an internal template VM is created and domain-joined (one reboot here, so clones need none later); replica VMs (thin-provisioned linked clones) are based on the template; a snapshot of each replica creates one running parent VM per ESXi host per datastore. At provisioning the parent VM is quiesced and 'forked', sharing its memory and disk read-only to spawn the clones. Each clone gets its own MAC/UUID via ClonePrep (AD join with no reboot, password change, license activation), then shares the replica's disk/memory read-only while all writes go to a delta disk. Clones are instantly powered-on; on logout the VM is deleted and recreated. No database needed, up to 2000 VMs per pool, lower vCenter load. Dated specifics, durable mechanism.

*Bron: blogpost 'VMware's Instant Clones technology with a touch of XenDesktop' (2017-01-17), basvankaam.com.*

## Verwante notities

- [Instant Clones are for non-persistent floating VDI only](instant-clones-use-case-and-limits.md)
- [MCS desktop types: pooled-random, pooled-static, dedicated](mcs-desktop-types-pooled-dedicated.md)
- [How Citrix MCS provisions VMs: snapshot, differencing disk, identity disk](mcs-how-it-works-disks.md)
- [Non-persistent plus layering = the best of both worlds](non-persistent-feels-persistent-with-layering.md)
- [Nutanix data locality and shadow clones for VDI](nutanix-data-locality-shadow-clones.md)
- [Personal vDisk: persistence of dedicated, manageability of pooled](personal-vdisk-pvd-concept.md)
- [PVS vs MCS image-delivery tradeoffs (XenDesktop 7 era)](pvs-vs-mcs-tradeoffs.md)
- [VMware Cloud Pod Architecture aggregates pods behind one entitlement layer](vmware-cloud-pod-architecture.md)
