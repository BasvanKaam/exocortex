---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-11
tags: [fslogix, application-layering, user-profile, vhd, wvd, vdi, rdsh, onedrive]
layer: reference
gedateerd: nee
bron: cgit-blog
---

# Profile Layering with FSLogix: Mount Instead of Copy

The most-used and most efficient answer to roaming-profile pain is layering. A separate virtual layer (a virtual disk, VHD/VHDX) holds the user's profile. At logon this layer is attached/mounted to the Windows OS, making the profile and its data available almost immediately.

Instead of copying the profile and sending it over the network, the whole profile is mounted to the machine as a disk mount of the VHD. All data is directly accessible: faster and far more efficient. Because the VHD is mounted at every logon and all profile changes are saved into it, the data appears persistent while in reality it 'roams' with the user.

The underlying technology is very complex, but conceptually it is a mount. The leading solution in this category is FSLogix, acquired by Microsoft not long ago and now a standard part of the Windows Virtual Desktop proposition. Besides profile data, these solutions also help applications that store data or configuration inside the profile, such as OneDrive.

*Bron: Salomon-IT 'Een technisch sales verhaal - deel 2 gebruiker profielen, data en uitdagingen' (CGIT Blogs).*

## Verwante notities

- [FSLogix: The Five Capabilities Bas Teaches](fslogix-five-capabilities.md)
- [FSLogix: the three core technologies after the Microsoft acquisition](fslogix-three-core-technologies.md)
- [Migrating homefolders and profiles to OneDrive with ShareGate](migrate-homefolders-profiles-to-onedrive-sharegate.md)
- [Non-persistent plus layering = the best of both worlds](non-persistent-feels-persistent-with-layering.md)
- [Office 365 on VDI/RDSH: .OST Bloat and the Search-Index Problem](office365-profile-pain-ost-and-search-index.md)
- [Outlook Online Mode Is Insufficient on VDI/RDSH](outlook-online-mode-insufficient-on-vdi.md)
- [Profile Disk plus VHD container: containerizing the user profile](profile-disk-vhd-container-concept.md)
- [Profile-on-VHD vs copy-on-login roaming profiles](profile-on-vhd-vs-copy-on-login.md)
- [User Profiles on VDI/RDSH: Bloat, Corruption and Roaming Challenges](user-profiles-roaming-challenges.md)
