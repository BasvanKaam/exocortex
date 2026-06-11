---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [windows, profiles, ntuser-dat, roaming-profile, terminal-server]
layer: reference
gedateerd: nee
bron: core-knowledge-docs
---

# How a Windows user profile loads

At logon the profile is loaded into HKEY_CURRENT_USER in the registry from NTuser.dat. At logoff any changed data in that hive is written back to the user's profile folder.

If the profile is stored somewhere other than the default location, it is always copied to the user's %systemroot%\profiles folder before being loaded into the registry. This is the **locally cached profile**, an important factor in Terminal Services because it affects logon time and consistency across servers.

The HKCU-from-NTUSER.DAT loading model is a durable Windows concept.

*Bron: Core Knowledge doc 'TS, Mem Usage, Shadow Key and (Flex) Profile Core Doc' (Bas zijn vroege sysadmin-naslag).*

## Verwante notities

- [Citrix / Terminal Services logon sequence (reference)](citrix-ts-logon-sequence.md)
- [Flex Profiles and PowerFuse profile storage (reference)](flex-profiles-powerfuse-profile-storage.md)
- [Hybrid user profiles vs roaming profiles](hybrid-user-profiles-explained.md)
- [Last write wins: why roaming profiles collide across sessions](last-write-wins-ntuser-dat.md)
- [PowerFuse Instant LogOff (reference)](powerfuse-instant-logoff.md)
- [Profile Portability: an abstraction layer over the user profile](profile-portability-abstraction-engine.md)
- [Terminal Server registry mapping and the load-balancing timestamp trap](terminal-server-registry-mapping-timestamp-trap.md)
- [Terminal Server AppSetup key and UsrLogon.cmd (reference)](ts-appsetup-key-and-usrlogon.md)
- [Windows user profile versions are incompatible across OS releases](windows-user-profile-version-incompatibility.md)
