---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-11
tags: [office-365, vdi, rdsh, outlook, ost, search-index, non-persistent]
layer: reference
gedateerd: ja
bron: cgit-blog
---

# Office 365 on VDI/RDSH: .OST Bloat and the Search-Index Problem

Mail delivered from the Azure cloud via Office 365 is now the rule rather than the exception, which adds specific challenges on VDI/RDSH, especially with non-persistent VMs (machine reset/wiped at logoff, or profile detached and deleted, erasing all changes and data).

## Challenge 1: .OST bloat (cached/offline mode)
Outlook can run online or offline (cached). Online mode (working live in the Azure cloud) in practice works insufficiently. Offline/cached mode copies a configurable amount of mail (e.g. last 3 or 6 months) locally into an .OST file, and that file lands inside the user profile. This grows the profile substantially (likely multiple GB), so the next logon to VDI/RDSH takes longer because the larger profile must load again.

## Challenge 2: search index reset
The Windows search index indexes data in the background at logon, including mailbox data in the profile. Because the profile and its data are deleted at logoff/reset every time, indexing starts over each session. Immediately after logon you have an unindexed inbox: Outlook search is near useless until indexing completes, and auto-complete of previously used names/addresses (also stored in the profile) is gone.

*Bron: Salomon-IT 'Een technisch sales verhaal - deel 2 gebruiker profielen, data en uitdagingen' (CGIT Blogs).*

## Verwante notities

- [Citrix WEM/UPM per-user Outlook search + OST roaming (Synergy 2018)](citrix-wem-upm-ost-search-roaming-2018.md)
- [Physical and performance limits of working from the cloud](cloud-physical-and-performance-limits.md)
- [FSLogix benefits for WVD (and on-premises)](fslogix-benefits-for-wvd-and-on-premises.md)
- [FSLogix: The Five Capabilities Bas Teaches](fslogix-five-capabilities.md)
- [Migrating homefolders and profiles to OneDrive with ShareGate](migrate-homefolders-profiles-to-onedrive-sharegate.md)
- [Office 365 cached mode breaks on non-persistent VDI/RDSH](office365-cached-mode-nonpersistent-problem.md)
- [Office 365 Network Performance: Service Front Doors and the Basics](office365-network-performance-basics.md)
- [Office 365 pain on non-persistent VDI, solved by containers](office365-nonpersistent-vdi-fslogix.md)
- [Outlook Online Mode Is Insufficient on VDI/RDSH](outlook-online-mode-insufficient-on-vdi.md)
- [Profile Layering with FSLogix: Mount Instead of Copy](profile-layering-fslogix.md)
- [User Profiles on VDI/RDSH: Bloat, Corruption and Roaming Challenges](user-profiles-roaming-challenges.md)
