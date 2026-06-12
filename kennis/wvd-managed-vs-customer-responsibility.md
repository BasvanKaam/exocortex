---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [wvd, azure, high-availability, shared-responsibility]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# WVD: what Microsoft makes HA vs what you must

How it worked in 2020: Windows Virtual Desktop is an Azure-native service hosted and managed by Microsoft. The control plane (database, web portal, brokering, load balancing of user connections) is Microsoft's to host, update and make highly available. You cannot and need not act on those.

What remains your responsibility: your session-host VMs and your data. That is where Availability Sets/Zones (for VMs) and storage redundancy (for Azure Files data) come in.

Nuance for non-persistent pools: many WVD deployments use non-persistent VMs storing no local data, so VM-level zone redundancy can be overkill (depends on RPO) since hosts are recreatable from a master image. Persistent, personally-assigned VMs are the opposite case and need real HA. (WVD has since been renamed Azure Virtual Desktop; the shared-responsibility split still holds.)

*Bron: blogpost 'How to Make Your 1,000+ User WVD Deployment Highly Available' (2020-12-07), basvankaam.com.*

## Verwante notities

- [Azure Availability Sets vs Availability Zones](azure-availability-sets-vs-zones.md)
- [Azure Files storage redundancy: LRS, ZRS, GRS](azure-files-storage-redundancy-lrs-zrs-grs.md)
- [Early WVD architecture: Microsoft-managed PaaS control plane + reverse connect](early-wvd-architecture-control-plane.md)
- [Nerdio shines where Microsoft's WVD HA docs are missing](nerdio-fills-microsoft-wvd-ha-doc-gap.md)
- ["One is none, two is one" -- but HA is a policy decision, not a dogma](one-is-none-but-it-depends.md)
- [WVD App Group rules (2019)](wvd-app-groups-rules-2019.md)
- [Even with managed WVD, the customer still owns the base image](wvd-customer-still-owns-the-base-image.md)
- [FSLogix Profile Containers as the WVD profile standard (2019)](wvd-profiles-fslogix-azure-files-2019.md)
- [WVD user connection flow and Reverse Connect](wvd-user-connection-flow-and-reverse-connect.md)
