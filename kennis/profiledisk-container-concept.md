---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [profiledisk, vhd, containers, user-profile, liquidware]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# ProfileDisk: redirect the whole profile to a VHD/VMDK container

How it worked then (Liquidware ProfileDisk, 2018): the entire user profile, including the registry, is redirected to a virtual disk file (VHD or VMDK). At login the profile disk is created/attached and connected to the OS just before the user enters credentials, so the OS immediately sees the profile as local and does not load a default profile.

Key benefit: all profile data lives as a single file instead of hundreds of separate files and folders, eliminating the per-file SMB/CIFS overhead (open, read, write, close, negotiate per file) that folder redirection plus roaming profiles incur. Data is available almost instantly after login, which is why containers suit large profiles. Bas calls it the profile 'Easy Button'. This is the same architectural idea that FSLogix later popularized as the dominant approach for Azure Virtual Desktop. Folder redirection can still be layered on top for certain shell folders as a best practice.

*Bron: blogpost 'The Easy Button - Corruption, Portability, Office 365, User Profile bloat, ProfileDisk, non-persistent Data Indexing and more' (2018-01-14), basvankaam.com.*

## Verwante notities

- [FlexApp 6.5: filter drivers replace symbolic links, broadening layering support](flexapp-filter-driver-vs-symbolic-links.md)
- [Last write wins: why roaming profiles collide across sessions](last-write-wins-ntuser-dat.md)
- [Office 365 pain on non-persistent VDI, solved by containers](office365-nonpersistent-vdi-fslogix.md)
- [Profile Disk plus VHD container: containerizing the user profile](profile-disk-vhd-container-concept.md)
- [Profile Portability: an abstraction layer over the user profile](profile-portability-abstraction-engine.md)
- [ProfileUnity saving direct to object cloud storage (no SMB file shares)](profileunity-direct-to-object-cloud-storage-2018.md)
- [FSLogix Profile Containers as the WVD profile standard (2019)](wvd-profiles-fslogix-azure-files-2019.md)
