---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [user-profiles, hybrid-profiles, roaming-profiles, logon-performance]
layer: reference
gedateerd: nee
bron: basvankaam-blog
---

# Hybrid user profiles vs roaming profiles

How it works: hybrid profile solutions store the user's personalized data in a per-user file on a file share, combined with a small, fast mandatory profile. At logon, the personalized HKCU registry data is read from that file separately from the logon process itself, so it doesn't slow logon the way large (and potentially corrupt) roaming profiles do.

Key advantage over roaming profiles: the admin chooses which data gets written back (e.g. only Office settings plus a couple of in-house apps). You can even pre-configure apps, export their HKCU registry settings and import them into the personalized profile file. Because read/write of personal data is isolated from logon/logoff, the process is much faster and you avoid most corrupt profiles. (Concept is durable; the contrast is with roaming profiles writing back the whole HKCU hive at logoff.)

*Bron: blogpost 'Microsoft's Windows XP is hot! Read why.' (2013-11-25), basvankaam.com.*

## Verwante notities

- [Flex Profiles and PowerFuse profile storage (reference)](flex-profiles-powerfuse-profile-storage.md)
- [Last write wins: why roaming profiles collide across sessions](last-write-wins-ntuser-dat.md)
- [Profile Disk plus VHD container: containerizing the user profile](profile-disk-vhd-container-concept.md)
- [Profile Portability: an abstraction layer over the user profile](profile-portability-abstraction-engine.md)
- [Why adding new farm servers can wipe user app settings (shadow key timestamps)](shadow-key-new-farm-server-timestamp-trap.md)
- [User Environment Management belongs on every workspace, not only virtual](uem-spans-physical-and-virtual.md)
- [Multi-site brokering is easy, user-data locality is the catch](user-data-locality-is-the-catch-in-multisite.md)
- [User Profiles on VDI/RDSH: Bloat, Corruption and Roaming Challenges](user-profiles-roaming-challenges.md)
- [How a Windows user profile loads](windows-roaming-profile-loading.md)
- [Windows user profile versions are incompatible across OS releases](windows-user-profile-version-incompatibility.md)
- [Granular profile handling: write-by-application-level and registry injection](write-by-application-level-profiles.md)
