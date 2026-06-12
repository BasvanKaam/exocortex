---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [office365, outlook, onedrive, vdi, rdsh, profiles]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Office 365 cached mode breaks on non-persistent VDI/RDSH

How it worked then (2017). Office 365 Outlook/Exchange can run in Exchange Online (all data in Azure, needing a constant connection, which in practice rarely gives the desired result) or cached mode (data downloaded into the AppData folder of the user profile on first open/login). Cached mode is by far the most implemented. On a traditional PC or a persistent VM this is fine: data is fetched once, then only deltas sync. The problem appears on non-persistent (stateless) VDI, RDSH, XenApp or Horizon View where the profile is only stored temporarily, especially Hosted Shared Desktops with many users per system. There, all Office 365 / Outlook data (and the data indexing) must be re-downloaded every login, causing very long logon times, lost productivity and user frustration.

*Bron: blogpost 'Probleem - Office 365: Outlook en OneDrive hebben een persistente opslaglocatie nodig' (2017-10-30), basvankaam.com.*

## Verwante notities

- [Citrix WEM/UPM per-user Outlook search + OST roaming (Synergy 2018)](citrix-wem-upm-ost-search-roaming-2018.md)
- [FSLogix Cloud Cache (tech preview, 2018)](fslogix-cloud-cache-2018.md)
- [The non-persistent Office 365 / Outlook OST and search-index problem](non-persistent-outlook-search-ost-problem.md)
- [Office 365 cached-mode OST files break on non-persistent desktops](office-365-ost-non-persistent-vdi-problem.md)
- [Office 365 pain on non-persistent VDI, solved by containers](office365-nonpersistent-vdi-fslogix.md)
- [Office 365 on VDI/RDSH: .OST Bloat and the Search-Index Problem](office365-profile-pain-ost-and-search-index.md)
- [Outlook Online Mode Is Insufficient on VDI/RDSH](outlook-online-mode-insufficient-on-vdi.md)
- [FSLogix Profile Containers as the WVD profile standard (2019)](wvd-profiles-fslogix-azure-files-2019.md)
