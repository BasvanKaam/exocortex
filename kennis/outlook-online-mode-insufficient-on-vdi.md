---
type: positie
merk: bvk
domein: cloud
status: actief
datum: 2026-06-11
tags: [office365, outlook, vdi, rdsh, stance, cached-mode]
bron: cgit-blog
---

# Outlook Online Mode Is Insufficient on VDI/RDSH

Bas takes a clear practical stance: running Outlook in pure online mode (working live against the Azure cloud) does not work well enough in practice on VDI/RDSH. The realistic path is cached/offline mode, which then forces you to deal with the downstream consequence, an .OST file inside the profile that bloats it and slows logons. The implication of his argument is that you cannot avoid the profile-management problem by going online-only; you must solve profiles properly (layering/FSLogix) instead.

*Bron: Salomon-IT 'Een technisch sales verhaal - deel 2 gebruiker profielen, data en uitdagingen' (CGIT Blogs).*

## Verwante notities

- [Citrix WEM/UPM per-user Outlook search + OST roaming (Synergy 2018)](citrix-wem-upm-ost-search-roaming-2018.md)
- [The non-persistent Office 365 / Outlook OST and search-index problem](non-persistent-outlook-search-ost-problem.md)
- [Office 365 cached mode breaks on non-persistent VDI/RDSH](office365-cached-mode-nonpersistent-problem.md)
- [Office 365 on VDI/RDSH: .OST Bloat and the Search-Index Problem](office365-profile-pain-ost-and-search-index.md)
- [Profile Layering with FSLogix: Mount Instead of Copy](profile-layering-fslogix.md)
