---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [terminal-server, registry, shadow-key, timestamps, load-balancing, citrix]
layer: reference
gedateerd: ja
bron: core-knowledge-docs
---

# Terminal Server registry mapping and the load-balancing timestamp trap

The server decides whether a logging-on user needs settings from the shadow area by comparing timestamps. While in install mode, each echo to the shadow key updates a `LatestRegistryKey` timestamp under `...\Terminal Server\Install\IniFile Times` (seconds since 1 Jan 1970). At logon, userinit.exe compares that hidden IniFile Times timestamp against the user's `HKCU\...\Terminal Server\LastUserIniSyncTime`. If the shadow area is newer, userinit enumerates the shadow keys, and for any key newer than the user's matching HKCU\Software key, deletes the user's key so they receive the shadow version ("Terminal Server registry mapping").

**The trap**: when you add fresh servers to a farm and install an application (e.g. Office) on them, the new shadow key timestamps are current, hence newer than every user's HKCU timestamps. Users load-balanced onto a new server have their app-specific HKCU\Software keys mass-deleted, and their settings appear to revert to defaults.

The shadow key cannot be disabled, so workarounds: set the new server's clock back before the original install time before installing; deploy the new server from an image of an old one (Ghost/sysprep/broken mirror, not an unattended install which writes current dates); or delete the keys from the new server's shadow area and use a logon script to populate new users' HKCU.

Dated TS internals, but captures Bas's own diagnosis of a real farm-expansion failure mode.

*Bron: Core Knowledge doc 'TS, Mem Usage, Shadow Key and (Flex) Profile Core Doc' (Bas zijn vroege sysadmin-naslag).*

## Verwante notities

- [Why adding new farm servers can wipe user app settings (shadow key timestamps)](shadow-key-new-farm-server-timestamp-trap.md)
- [Shadow key behavior on 64-bit and TSAWARE apps](shadow-key-wow64-and-tsaware.md)
- [Terminal Server install vs execute mode and the shadow key (reference)](terminal-server-install-vs-execute-mode-shadow-key.md)
- [The Terminal Server shadow key and registry sync at logon](terminal-server-shadow-key.md)
- [Terminal Server / Citrix troubleshooting checklist (own notes)](terminal-server-troubleshooting-checklist.md)
- [How a Windows user profile loads](windows-roaming-profile-loading.md)
