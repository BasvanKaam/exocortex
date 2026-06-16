---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [xendesktop, host-connection, mcs, pvs, scvmm, hypervisor]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# XenDesktop 7 Host Infrastructure and what it unlocks

How it worked then: in XenDesktop 7 Studio, the Host Infrastructure is the bridge to the underlying hypervisor (Hyper-V, vSphere or XenServer) where VMs run. Because Studio must start/stop/create/delete/monitor VMs, it needs the hypervisor's management layer: SCVMM for Hyper-V, vCenter for VMware, XenCenter for XenServer. Studio talks to the hypervisor APIs through it.

Configuring a Host Infrastructure is optional but gates capability: without it you cannot use MCS or PVS to mass-provision VMs from a golden image, and the Machine Catalog wizard greys out virtual-hardware and MCS options. MCS only works with virtual machines; PVS can stream physical workloads (its original design) even without a Host Infrastructure. The PVS XenDesktop Setup Wizard requires a Host Infrastructure.

Gotcha he hit: in the SCVMM connection, the username must include the domain suffix (domain\username) or the wizard errors.

*Bron: blogpost 'How to... Install and configure your Host Infrastructure' (2013-11-17), basvankaam.com.*

## Verwante notities

- [Citrix Validated Solution: XenDesktop on Nutanix reference architecture](citrix-validated-solution-nutanix.md)
- [How Citrix MCS provisions VMs: snapshot, differencing disk, identity disk](mcs-how-it-works-disks.md)
- [VDI-in-a-Box: the simplified all-in-one VDI appliance](vdi-in-a-box-architecture.md)
- [VIAB vs XenDesktop: simplicity vs flexibility tradeoffs (2013)](viab-vs-xendesktop-tradeoffs.md)
