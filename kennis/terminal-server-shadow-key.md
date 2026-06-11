---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [terminal-server, registry, shadow-key, rds, citrix]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# The Terminal Server shadow key and registry sync at logon

How it worked then (Terminal Server / XenApp era, 32-bit and Server 2008R2).

A Terminal Server runs in one of two modes: install mode (set via `change user /install` or Add/Remove Programs) or execute mode (the normal 99%-of-the-time state where users launch published apps).

When an app is installed in install mode, every write it makes to the installing admin's `HKCU\Software` hive is also echoed to the shadow key at `HKLM\Software\Microsoft\Windows NT\CurrentVersion\Terminal Server\Install\Software`. This happens per application and per key. Each write also updates a `LatestRegistryKey` timestamp under `...\Terminal Server\Install\IniFile Times` (seconds since 1 Jan 1970), and every individual key carries its own timestamp.

At logon, `userinit.exe` compares the server's IniFile Times timestamp with the user's `HKCU\...\Terminal Server\LastUserIniSyncTime`. If the server side is newer, it enumerates the shadow keys, and for each key newer than the user's copy it deletes the user's key and replaces it with the shadow version. Keys it cannot find in the user hive (fresh profile, new app) get copied over. This is the mechanism that gets per-app initial config from the installing admin's profile into every user's profile.

*Bron: blogpost 'The Shadow Key: what's it all about?!' (2012-12-23), basvankaam.com.*

## Verwante notities

- [Why adding new farm servers can wipe user app settings (shadow key timestamps)](shadow-key-new-farm-server-timestamp-trap.md)
- [Shadow key behavior on 64-bit and TSAWARE apps](shadow-key-wow64-and-tsaware.md)
