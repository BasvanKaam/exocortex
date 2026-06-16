---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [wvd, fslogix, profile-container, azure-files]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# FSLogix Profile Containers as the WVD profile standard (2019)

How it stood in 2019:

- FSLogix Profile Containers would be the only supported profile solution going forward. CSPs (including Citrix) were not allowed to use anything else.
- Storage Spaces Direct was the preferred container store at the time; Azure Files was coming and would become preferred. Azure storage must be used for WVD profiles.
- UPD and Roaming Profiles would eventually no longer be supported; a UPD migration script was promised.
- Sizing guidance: plan 5-15 GB per user; 5-15 IOPS per user; 70% write, 30% read.
- Best practice: configure Profile Containers on a per-hostpool basis.

*Bron: blogpost '49 facts listed - What I picked up during a WVD Solution Design Workshop' (2019-05-13), basvankaam.com.*

## Verwante notities

- [Azure Ephemeral OS disks for stateless WVD workloads](azure-ephemeral-os-disks.md)
- [Azure Files storage redundancy: LRS, ZRS, GRS](azure-files-storage-redundancy-lrs-zrs-grs.md)
- [FSLogix benefits for WVD (and on-premises)](fslogix-benefits-for-wvd-and-on-premises.md)
- [FSLogix Cloud Cache (tech preview, 2018)](fslogix-cloud-cache-2018.md)
- [Microsoft has never managed profiles and desktop UX well](microsoft-weak-at-user-data-and-desktop-experience.md)
- [MSIX app attach: VHD-mounted apps via FSLogix filter drivers](msix-app-attach-concept.md)
- [WVD prerequisites Nerdio still relies on: AD sync and FSLogix profiles](nerdio-wvd-prerequisites-ad-fslogix.md)
- [Office 365 cached mode breaks on non-persistent VDI/RDSH](office365-cached-mode-nonpersistent-problem.md)
- [Office 365 pain on non-persistent VDI, solved by containers](office365-nonpersistent-vdi-fslogix.md)
- [ProfileDisk: redirect the whole profile to a VHD/VMDK container](profiledisk-container-concept.md)
- [Even with managed WVD, the customer still owns the base image](wvd-customer-still-owns-the-base-image.md)
- [WVD: what Microsoft makes HA vs what you must](wvd-managed-vs-customer-responsibility.md)
- [Windows Virtual Desktop: multi-user Windows 10 as DaaS on Azure](wvd-multi-user-windows10-daas-2019.md)
- [WVD preview constraints (2019)](wvd-preview-good-to-knows.md)
- [WVD introduced multi-user Windows 10 and a license-based entitlement model](wvd-win10-multiuser-and-licensing.md)
