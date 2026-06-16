---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [vdi-in-a-box, citrix, vdi, flexcast]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# VDI-in-a-Box: the simplified all-in-one VDI appliance

How it worked then: VIAB was Citrix's simplified XenDesktop for small/mid-sized companies, though Bas notes deployments reaching 500+ and even thousands of VMs. It's a single virtual appliance (vdiManager) bundling connection broker, user manager, load balancer and desktop provisioning server.

- No shared storage required (optional), no SCVMM/XenCenter/vCenter, no management servers or high-speed links; runs on commodity hardware with XenServer, Hyper-V or VMware. Uses existing AD or a workgroup. Managed from one web console.
- Can run as a single server or as a Grid (multiple vdiManager servers) for load balancing and HA.
- Only one FlexCast delivery model: VDI (hence the name), versus XenDesktop's full set (Streamed VHD, Local VM, VDI, Hosted Shared, On-Demand Apps).
- Provisioning: imports a pre-built VM as base image, then templates + policies create desktops. Pooled VMs get a linked-clone VHD; personal VMs add a Personal vDisk VHD for delta writes. No PVS/MCS, no image versioning. Policies must live in AD.

Bas's verdict: 'its simplicity is also its strength.'

*Bron: blogpost 'VIAB and Windows Server 2012 R2's Data Deduplication' (2013-11-20), basvankaam.com.*

## Verwante notities

- [Personal vDisk: persistence of dedicated, manageability of pooled](personal-vdisk-pvd-concept.md)
- [Server 2012 R2 data dedup and the VDI separation rule](server-2012-r2-dedup-for-vdi.md)
- [VDI-in-a-Box: a single all-in-one VDI appliance (how it worked)](vdi-in-a-box-all-in-one-appliance.md)
- [VDI-in-a-Box served a real niche: simple, cheap, small-scale VDI](vdi-in-a-box-simple-vdi-niche.md)
- [VIAB isn't for everyone, but with the right business case it just feels right (May 2013)](viab-given-the-right-business-case-it-feels-right.md)
- [Simplicity is a feature, not a drawback (VIAB)](viab-simplicity-is-strength-position.md)
- [VIAB vs XenDesktop: simplicity vs flexibility tradeoffs (2013)](viab-vs-xendesktop-tradeoffs.md)
- [XenDesktop 7 Host Infrastructure and what it unlocks](xendesktop-host-infrastructure-mcs-pvs.md)
