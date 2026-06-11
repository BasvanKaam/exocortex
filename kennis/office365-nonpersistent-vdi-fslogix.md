---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [office365, vdi, fslogix, non-persistent]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Office 365 pain on non-persistent VDI, solved by containers

Running Office 365 on non-persistent (pooled) desktops, and on SBC/RDS, caused real problems c. 2017 because data lives in the Azure cloud and you traverse the internet to reach it: poor performance and time-outs opening mail or calendar items, and very slow inbox/folder search. Workarounds existed but were far from ideal.

FSLogix Office 365 Containers were the go-to fix, letting you take full advantage of VDI/SBC workloads. (FSLogix was later acquired by Microsoft and became core to FSLogix profile/Office containers.)

How it worked then; the underlying search-index/profile problem on non-persistent desktops remains a durable concern.

*Bron: blogpost 'A few 'State of the VDI and SBC union' results in more detail' (2017-07-23), basvankaam.com.*

## Verwante notities

- [FSLogix Cloud Cache (tech preview, 2018)](fslogix-cloud-cache-2018.md)
- [FSLogix is not an application layering company; App Disks are doomed](fslogix-not-an-app-layering-company.md)
- [The non-persistent Office 365 / Outlook OST and search-index problem](non-persistent-outlook-search-ost-problem.md)
- [Office 365 cached-mode OST files break on non-persistent desktops](office-365-ost-non-persistent-vdi-problem.md)
- [Office 365 cached mode breaks on non-persistent VDI/RDSH](office365-cached-mode-nonpersistent-problem.md)
- [Profile Disk plus VHD container: containerizing the user profile](profile-disk-vhd-container-concept.md)
- [ProfileDisk: redirect the whole profile to a VHD/VMDK container](profiledisk-container-concept.md)
- [FSLogix Profile Containers as the WVD profile standard (2019)](wvd-profiles-fslogix-azure-files-2019.md)
