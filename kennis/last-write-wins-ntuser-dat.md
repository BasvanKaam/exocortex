---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [roaming-profiles, ntuser-dat, user-profile, rdsh]
layer: reference
gedateerd: nee
bron: basvankaam-blog
---

# Last write wins: why roaming profiles collide across sessions

NTUSER.DAT holds a user's HKCU registry hive (personal and application settings) but the OS treats it as a single file. On logoff the file is copied back to the central share and overwrites the existing copy because timestamps are compared. With multiple concurrent sessions on multiple machines, the profile loads at least twice; when session 1 ends its NTUSER.DAT is written back, then when session 2 ends it overwrites those settings. The most recent write wins, so changes from the earlier-closing session are silently lost.

Mandatory profiles avoid this because all users share a read-only NTUSER.MAN that is never written back. The problem becomes common with RDSH multi-user setups, published applications, and workspace aggregators where having more than one active copy of a profile at the same time is routine.

*Bron: blogpost 'The last write wins - NO, it does not, we do!' (2017-12-04), basvankaam.com.*

## Verwante notities

- [Hybrid user profiles vs roaming profiles](hybrid-user-profiles-explained.md)
- [ProfileDisk: redirect the whole profile to a VHD/VMDK container](profiledisk-container-concept.md)
- [Why adding new farm servers can wipe user app settings (shadow key timestamps)](shadow-key-new-farm-server-timestamp-trap.md)
- [Shadow key behavior on 64-bit and TSAWARE apps](shadow-key-wow64-and-tsaware.md)
- [Windows user profile versions are incompatible across OS releases](windows-user-profile-version-incompatibility.md)
- [Granular profile handling: write-by-application-level and registry injection](write-by-application-level-profiles.md)
