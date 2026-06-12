---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [fslogix, cloud-cache, profile-containers, office365, azure, s3, resiliency]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# FSLogix Cloud Cache (tech preview, 2018)

How it was presented then (E2EVC Amsterdam, June 2018, by Benny and Jim): FSLogix Cloud Cache builds on the existing Profile and Office 365 containers. It lets profile data be stored in multiple locations at once, local device, traditional on-premises SMB shares, and public cloud storage, with no SMB infrastructure needed because it interacts directly with cloud-based storage REST APIs. At the time it was in tech preview, due to go GA within weeks. Existing container customers would get limited functionality (one storage location plus local cache) for free; multiple storage locations would cost extra. Azure block storage was first in line at GA, with S3 (AWS) to follow.

The durable concept: replicating the profile container across multiple backends (local + on-prem + cloud) for resiliency and portability, without an SMB file server, via storage REST APIs. Note the parallel: Liquidware ProfileUnity demoed the same direct-to-cloud-storage idea at the same event, the whole industry was converging on SMB-less, API-driven profile storage in 2018.

*Bron: blogpost 'E2EVC (Epic edition) Amsterdam is a wrap - notes, announcements, video's & photo's' (2018-06-11), basvankaam.com.*

## Verwante notities

- [Citrix's native options still lag third-party containers (May 2018)](citrix-still-behind-third-party-containers-2018.md)
- [E2EVC as a flat, high-value community conference](e2evc-community-conference-value.md)
- [FSLogix benefits for WVD (and on-premises)](fslogix-benefits-for-wvd-and-on-premises.md)
- [FSLogix: The Five Capabilities Bas Teaches](fslogix-five-capabilities.md)
- [FSLogix is not an application layering company; App Disks are doomed](fslogix-not-an-app-layering-company.md)
- [Office 365 cached mode breaks on non-persistent VDI/RDSH](office365-cached-mode-nonpersistent-problem.md)
- [Office 365 pain on non-persistent VDI, solved by containers](office365-nonpersistent-vdi-fslogix.md)
- [ProfileUnity saving direct to object cloud storage (no SMB file shares)](profileunity-direct-to-object-cloud-storage-2018.md)
- [Multi-site brokering is easy, user-data locality is the catch](user-data-locality-is-the-catch-in-multisite.md)
- [Windows Virtual Desktop: multi-user Windows 10 as DaaS on Azure](wvd-multi-user-windows10-daas-2019.md)
- [FSLogix Profile Containers as the WVD profile standard (2019)](wvd-profiles-fslogix-azure-files-2019.md)
