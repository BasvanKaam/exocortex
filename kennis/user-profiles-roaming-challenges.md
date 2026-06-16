---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-11
tags: [user-profile, vdi, rdsh, roaming-profile, euc, wvd]
layer: reference
gedateerd: nee
bron: cgit-blog
---

# User Profiles on VDI/RDSH: Bloat, Corruption and Roaming Challenges

Every user has a profile, regardless of physical, virtual, single- or multi-user. The profile is a repository of personal settings: application and program settings the user changes, plus OS-related info (monitor configs, network connections, desktop background, favorites, file/folder history). Lose or corrupt a profile and a new empty default is created; you start over (e.g. Word loses your settings on next launch).

## The bloat problem
Profiles can grow significantly, from tens/hundreds of MB to multiple GB. On a normal PC/laptop this is fine: the profile sits on the local disk/SSD and is available almost instantly. On VDI/RDSH (Microsoft, Citrix, VMware, or other), the profile is generally stored centrally on a separate system (a File Server). At logon it is copied from there to the VDI/RDSH session: the bigger the profile, the longer this takes. This includes cloud environments, including Windows Virtual Desktop.

## Roaming Profiles
The whole copy-in-at-logon, copy-back-at-logoff concept is called Roaming Profiles. It is normal for a profile to be detached and deleted at logoff, so it must be copied/loaded again at every logon. VDI/RDSH architecture can cause a profile to not detach or clean up correctly, or to load multiple times simultaneously, which can corrupt the profile and make it unusable.

*Bron: Salomon-IT 'Een technisch sales verhaal - deel 2 gebruiker profielen, data en uitdagingen' (CGIT Blogs).*

## Verwante notities

- [Hybrid user profiles vs roaming profiles](hybrid-user-profiles-explained.md)
- [Migrating homefolders and profiles to OneDrive with ShareGate](migrate-homefolders-profiles-to-onedrive-sharegate.md)
- [Office 365 on VDI/RDSH: .OST Bloat and the Search-Index Problem](office365-profile-pain-ost-and-search-index.md)
- [Profile Layering with FSLogix: Mount Instead of Copy](profile-layering-fslogix.md)
- [Profile-on-VHD vs copy-on-login roaming profiles](profile-on-vhd-vs-copy-on-login.md)
- [How a Windows user profile loads](windows-roaming-profile-loading.md)
