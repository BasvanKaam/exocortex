---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [terminal-server, shadow-key, citrix-farm, registry, troubleshooting]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Why adding new farm servers can wipe user app settings (shadow key timestamps)

How it worked then. Adding fresh servers to an existing farm is a trap: the apps installed on the new servers generate newer shadow key timestamps than the user settings obtained from the original (older) servers. At logon to the new servers, the sync logic sees the newer timestamps and deletes/overwrites the user's app-specific config keys, losing their preferences.

The behavior cannot be disabled. The fix is to make the new servers' shadow key timestamps older than what users already carry. Three options, each with drawbacks:
1. Sysprep/image new servers so they inherit the original build's registry timestamps.
2. Write to HKCU\Software in install mode with the system clock set in the past.
3. Delete the shadow keys that could overwrite user preferences (preferred) and instead inject the config another way at logon (login script, AppSense / user environment management, etc.).

*Bron: blogpost 'The Shadow Key: what's it all about?!' (2012-12-23), basvankaam.com.*

## Verwante notities

- [Hybrid user profiles vs roaming profiles](hybrid-user-profiles-explained.md)
- [Last write wins: why roaming profiles collide across sessions](last-write-wins-ntuser-dat.md)
- [Forcing Microsoft Security Essentials onto Server 2012 (home lab)](mse-on-server-2012-workaround.md)
- [Shadow key behavior on 64-bit and TSAWARE apps](shadow-key-wow64-and-tsaware.md)
- [The Terminal Server shadow key and registry sync at logon](terminal-server-shadow-key.md)
- [Windows user profile versions are incompatible across OS releases](windows-user-profile-version-incompatibility.md)
