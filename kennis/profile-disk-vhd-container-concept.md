---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [liquidware, profileunity, profile-disk, vhd, profile]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Profile Disk plus VHD container: containerizing the user profile

How it worked then. Liquidware ProfileUnity's Profile Disk combined with a VHD container solves the non-persistent Office 365 / large-profile problem by storing all user-related data on a virtual hard disk (.VHD or .VMDK, depending on hypervisor). At logon the disk is attached to the physical or virtual machine, 'like a puzzle piece that fits exactly and is easy to remove'. User data (and completed indexing) becomes available almost immediately after login or Outlook open, and the last state is preserved across logoff. It covers all Office 365 data including OneDrive for Business, Teams and OneNote, plus any other profile data. Each user gets their own Profile Disk / VHD container, usable in both single-user VDI and multi-user RDSH environments. Caveat (see the companion note): the profile on the disk is still bound to the underlying OS version unless combined with Profile Portability.

*Bron: blogpost 'Probleem - Office 365: Outlook en OneDrive hebben een persistente opslaglocatie nodig' (2017-10-30), basvankaam.com.*

## Verwante notities

- [Hybrid user profiles vs roaming profiles](hybrid-user-profiles-explained.md)
- [Liquidware suite: ProfileUnity, FlexApp, Stratusphere UX (2018)](liquidware-profileunity-flexapp-stratusphere.md)
- [The non-persistent Office 365 / Outlook OST and search-index problem](non-persistent-outlook-search-ost-problem.md)
- [Office 365 pain on non-persistent VDI, solved by containers](office365-nonpersistent-vdi-fslogix.md)
- [Profile Layering with FSLogix: Mount Instead of Copy](profile-layering-fslogix.md)
- [Profile-on-VHD vs copy-on-login roaming profiles](profile-on-vhd-vs-copy-on-login.md)
- [Profile Portability: an abstraction layer over the user profile](profile-portability-abstraction-engine.md)
- [ProfileDisk: redirect the whole profile to a VHD/VMDK container](profiledisk-container-concept.md)
- [ProfileUnity feature set and all-in-one model (2017)](profileunity-feature-overview-2017.md)
