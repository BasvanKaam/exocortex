---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [user-profile, vhd, fslogix, roaming-profile, vdi, rdsh, logon-performance]
layer: reference
gedateerd: nee
bron: cgit-blog
---

# Profile-on-VHD vs copy-on-login roaming profiles

A three-model explainer for how a Windows user profile is delivered to a VDI/RDSH session:

1. **Profile on VHD (container model).** The user's profile lives in a VHD on a file server. At logon the corresponding VHD is mounted/attached to the VDI/RDSH machine rather than copied. The key advantage: profile data is available almost immediately after logon because nothing is copied across the wire. (This is the FSLogix-style profile-container approach.)

2. **Local profile.** The profile sits on the machine's own HDD/SSD (a desktop or laptop). Nothing is copied at logon and data is immediately available because it never left the device.

3. **Traditional copy-on-login roaming profile.** The profile lives on a file server and is copied to the VDI/RDSH machine during logon. All data is only available once the copy action completes, which is the slow path the container model is designed to replace.

The core teaching point: mounting a VHD ('koppelen') beats copying ('kopieerslag') for logon speed and data availability.

*Bron: CGIT-deck 'User profile.pptx' speaker notes.*

*Bron: Salomon-IT 'User profile' (CGIT Blogs).*

## Verwante notities

- [FSLogix: the three core technologies after the Microsoft acquisition](fslogix-three-core-technologies.md)
- [Profile Disk plus VHD container: containerizing the user profile](profile-disk-vhd-container-concept.md)
- [Profile Layering with FSLogix: Mount Instead of Copy](profile-layering-fslogix.md)
- [User Profiles on VDI/RDSH: Bloat, Corruption and Roaming Challenges](user-profiles-roaming-challenges.md)
