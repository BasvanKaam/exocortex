---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [office365, outlook, ost, search-index, non-persistent, vdi, rdsh, profile]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# The non-persistent Office 365 / Outlook OST and search-index problem

How it worked then (2018): with Office 365 delivered on non-persistent workspaces (RDSH like XenApp, or pooled VDI VMs), the core problem was twofold. Online mode against Azure performed poorly, so Outlook was run in Offline (cached) mode, meaning the .OST file lived in the user's profile, bloating profiles and lengthening login times. Worse, because non-persistent machines store nothing locally, the Outlook search index had to be rebuilt on every login or reboot, a time- and resource-consuming process. The Windows Search index is machine-bound and cannot roam with the user.

This is the exact gap that container/profile solutions filled: FSLogix Profile and Office 365 containers, Liquidware ProfileDisk/VHD containers, Ivanti Environment Manager, and Citrix's own User/Office 365 layers. The durable lesson: stateless desktops plus a stateful, machine-bound search index is an inherent mismatch that needs an external container to bridge.

*Bron: blogpost 'Synergy 2018: Per-user Outlook search indexing and OST caching options' (2018-05-14), basvankaam.com.*

## Verwante notities

- [Citrix's native options still lag third-party containers (May 2018)](citrix-still-behind-third-party-containers-2018.md)
- [Citrix WEM/UPM per-user Outlook search + OST roaming (Synergy 2018)](citrix-wem-upm-ost-search-roaming-2018.md)
- [Non-persistent plus layering = the best of both worlds](non-persistent-feels-persistent-with-layering.md)
- [Office 365 cached-mode OST files break on non-persistent desktops](office-365-ost-non-persistent-vdi-problem.md)
- [Office 365 cached mode breaks on non-persistent VDI/RDSH](office365-cached-mode-nonpersistent-problem.md)
- [Office 365 pain on non-persistent VDI, solved by containers](office365-nonpersistent-vdi-fslogix.md)
- [Profile Disk plus VHD container: containerizing the user profile](profile-disk-vhd-container-concept.md)
- [Granular profile handling: write-by-application-level and registry injection](write-by-application-level-profiles.md)
