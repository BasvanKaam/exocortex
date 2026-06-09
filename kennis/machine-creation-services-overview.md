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
