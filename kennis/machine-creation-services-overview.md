---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [mcs, citrix, provisioning, xendesktop, fma]
layer: reference
bron: inside-citrix-fma
---

# Machine Creation Services (MCS): integrated single-image delivery

MCS is the second option (next to Provisioning Services) for automated desktop image delivery and single-image management within XenDesktop. Unlike PVS, it requires no separate infrastructure: it is integrated directly into XenDesktop and managed from Studio.

MCS communicates directly with the hypervisor's API to handle VM creation, power management (start/stop), deletion, and so on. It supports Microsoft Hyper-V (via SCVMM), VMware vSphere (via vCenter), and Citrix XenServer (by talking directly to the Pool master and/or XenCenter). It works on-premises and in the cloud.

Originally built for VDI-based VMs, as of XenDesktop 7 MCS also supports provisioning server operating systems. MCS is based on Differencing Disk technology, similar to VMware's Linked Clones. MCS can only provision virtual machines, never physical (use PVS for physical).

## Verwante notities

- [Citrix Host Connection](citrix-host-connection.md)
- [Citrix Project Accelerator: web-based design guidance](citrix-project-accelerator.md)
- [CWC authentication and credential handling security](cwc-authentication-credential-handling.md)
- [FMA Hypervisor Communications Library (HCL) abstraction layer](fma-hypervisor-communications-library.md)
- [Host Connection key takeaways: MCS/PVS and cloud support](host-connection-mcs-pvs-cloud-support-key-takeaways.md)
- [Host Connections now support cloud, not just hypervisors](host-connections-cloud-support.md)
- [Machine Creation Services essentials](machine-creation-services-essentials.md)
- [MCS desktop types: Pooled-Random, Pooled-Static, Dedicated](mcs-desktop-types.md)
- [MCS Differencing Disk and Identity Disk](mcs-differencing-and-identity-disk.md)
- [How Citrix MCS provisions VMs: snapshot, differencing disk, identity disk](mcs-how-it-works-disks.md)
- [MCS supported hypervisor storage and thin provisioning limits](mcs-hypervisor-storage-support.md)
- [Citrix Provisioning Services (PVS) overview](provisioning-services-overview.md)
- [Personal vDisks (PvD)](pvs-personal-vdisks-pvd.md)
- [PVS provisioning wizards: streamed VM and XenDesktop setup](pvs-provisioning-wizards.md)
- [Citrix Studio console root nodes](studio-console-root-nodes.md)
