---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [wow64, terminal-server, tsaware, server-2008r2, shadow-key]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Shadow key behavior on 64-bit and TSAWARE apps

How it worked then.

64-bit: there are two shadow key locations. A 32-bit app installed on a 64-bit system has its writes redirected by the WoW64 layer to `HKLM\Software\Wow6432Node\Microsoft\Windows NT\CurrentVersion\Terminal Server\Install`; a 64-bit app uses the non-redirected `...\Terminal Server\Install` location. At logon both are copied into the user hive, and when the 32-bit and 64-bit shadow keys conflict the 32-bit one wins.

Server 2008R2 and later (incl. Windows 8 / 2012): applications can be marked TSAWARE via a flag in the executable header. A TSAWARE app signals it does not need shadow key echoing, so nothing is copied to the shadow key location on install. Echoing only happens for executables NOT marked TSAWARE.

*Bron: blogpost 'The Shadow Key: what's it all about?!' (2012-12-23), basvankaam.com.*

## Verwante notities

- [Moving 32-bit to 64-bit (and 2003 to 2008) means app-compat work (durable lesson)](32bit-to-64bit-app-compat-is-a-fact-of-life.md)
- [Last write wins: why roaming profiles collide across sessions](last-write-wins-ntuser-dat.md)
- [Why adding new farm servers can wipe user app settings (shadow key timestamps)](shadow-key-new-farm-server-timestamp-trap.md)
- [The Terminal Server shadow key and registry sync at logon](terminal-server-shadow-key.md)
