---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [liquidware, profileunity, profile-portability, profilebridge, migration]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Profile Portability: an abstraction layer over the user profile

How it worked then. Liquidware ProfileUnity's Profile Portability (a.k.a. ProfileBridge) solves cross-OS profile incompatibility by treating the profile differently: its engine knows exactly where each piece of data lives in the profile (folders, config files, registry keys, per-application settings), in what form and what it is for, and builds an abstraction layer over it. On logoff the valuable data is compressed and written to a central network folder (step 1); on logon to a newer OS / newer profile version the engine reads that stored data back into the new profile (step 2). It works for every Windows profile/OS version and in both directions (old-to-new and new-to-old), enabling e.g. a Friday-on-Windows-7, Monday-on-Windows-10 migration with no lost settings, and handling recurring Windows 10 feature-update profile changes. Note: a Profile Disk alone does not solve this (the profile on it is still OS-bound); the unique combination is Profile Disk + Profile Portability, optionally with Context-aware Filters, Trigger Points, Folder Redirection and Privilege Elevation.

*Bron: blogpost 'Probleem - Windows 10 blijkt niet het beloofde 'One OS to rule them all'. Gebruikersprofiel versies blijven wijzigen' (2017-11-10), basvankaam.com.*

## Verwante notities

- [Don't start from scratch every OS update: vendor-neutral workspace layer](configure-once-migrate-many-vs-lockin.md)
- [Flex Profiles and PowerFuse profile storage (reference)](flex-profiles-powerfuse-profile-storage.md)
- [Hybrid user profiles vs roaming profiles](hybrid-user-profiles-explained.md)
- [Liquidware suite: ProfileUnity, FlexApp, Stratusphere UX (2018)](liquidware-profileunity-flexapp-stratusphere.md)
- [Profile Disk plus VHD container: containerizing the user profile](profile-disk-vhd-container-concept.md)
- [ProfileDisk: redirect the whole profile to a VHD/VMDK container](profiledisk-container-concept.md)
- [ProfileUnity feature set and all-in-one model (2017)](profileunity-feature-overview-2017.md)
- [Windows 10 was never the promised 'One OS to rule them all'](windows-10-not-one-os-to-rule-them-all.md)
- [Microsoft's 'one Windows 10 to rule them all' promise was false](windows-10-not-one-os-to-rule-them-all-2.md)
- [How a Windows user profile loads](windows-roaming-profile-loading.md)
- [Windows user profile versions are incompatible across OS releases](windows-user-profile-version-incompatibility.md)
- [Windows user profile versions are not cross-compatible](windows-user-profile-version-incompatibility-2.md)
- [Granular profile handling: write-by-application-level and registry injection](write-by-application-level-profiles.md)
