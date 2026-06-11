---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [microsoft, windows-server-2012r2, work-folders, sync, byod]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Work Folders: on-premises file sync as a Dropbox alternative

How it worked then: Work Folders (Windows Server 2012 R2) let users store and access corporate data on personal and corporate PCs and mobile devices from a single point, with offline access and sync when a connection returned, whether or not the device was domain-joined. It was enabled via the FS-SyncShareService feature (Add-WindowsFeature FS-SyncShareService) at no extra cost.

Key property and its durable point: the centralised storage was an on-premises Windows Server 2012 R2 file server, giving full control of the data, integrated into File Explorer, with quotas and data classification available. Unlike SkyDrive/ShareFile/Google Drive it held user data only and was intended for personal use. Client support at launch was limited to Windows 8.1 Preview and Windows RT 8.1 Preview. Bas's framing of the durable why: many organisations simply do not trust the cloud with corporate data, so an on-prem-controlled sync option matters.

*Bron: blogpost 'Mobility based on Windows Server 2012 R2' (2013-10-01), basvankaam.com.*

## Verwante notities

- [BYOD has graduated from hype to something you can't ignore](byod-from-hype-to-unavoidable.md)
- [2013 mobile management vendor landscape](byod-vendor-landscape-2013.md)
- [Chromebooks require an online state of mind](chromebook-online-state-of-mind.md)
- [Mobile management acronyms: MDM, MAM, MIM, EMM](mdm-mam-mim-emm-glossary.md)
- [Positie: Microsoft is closing the gap on VMware and Citrix](positie-microsoft-closing-the-gap-on-vmware-and-citrix.md)
- [SDN via Hyper-V network virtualization (how it worked in 2012 R2)](sdn-network-virtualization-2012r2.md)
- [ShareFile is miles ahead of the competition (2017 take)](sharefile-miles-ahead-of-competition.md)
- [Workplace Join: registering devices without full domain join](workplace-join-2012r2.md)
