---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, pvs, mcs, provisioning, xendesktop, image-management]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# PVS vs MCS image-delivery tradeoffs (XenDesktop 7 era)

How it worked around XenDesktop 7. Two ways to provision machines from a single image:

- **PVS (Provisioning Services)** is a stand-alone product needing its own server (virtual or physical) and a separate management console. Requires attention to DHCP/PXE/TFTP, though a BDM disk can replace that (see separate note). Offers enhanced image management and storage IO optimizations, beneficial in larger environments. Supports physical *and* virtual targets.
- **MCS (Machine Creation Services)** leverages the hypervisor's underlying storage directly, no separate infrastructure, no PXE/DHCP reconfiguration. Only supports virtual machines. As of XD7, MCS could use Hyper-V 3.0 Clustered Shared Volume Read Caching to cut storage IO during boot/logon storms (similar effect to PVS caching, blocks delivered once per Hyper-V host then shared among its VMs, using host RAM).

Rule of thumb Bas gave readers: PVS is the better choice for larger VDI/HSD deployments, but MCS is closing the gap and is fine in many cases depending on the rest of the infrastructure.

*Bron: blogpost 'Citrix Provisioning Services 7... A sneak preview' (2013-06-21), basvankaam.com.*

## Verwante notities

- [Instant Clones are for non-persistent floating VDI only](instant-clones-use-case-and-limits.md)
- [MCS desktop types: pooled-random, pooled-static, dedicated](mcs-desktop-types-pooled-dedicated.md)
- [How Citrix MCS provisions VMs: snapshot, differencing disk, identity disk](mcs-how-it-works-disks.md)
- [MCS planning: master-VM count x data-store count x update frequency](mcs-storage-and-update-cycle-cost.md)
- [MCS vs PVS is done to death; pick a lens and stress-test the choice](positie-mcs-not-vs-pvs.md)
- [How VMware Instant Clones (vmFork) provision desktops in seconds](vmware-instant-clones-vmfork-mechanics.md)
