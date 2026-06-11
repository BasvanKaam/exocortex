---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [flex-profiles, powerfuse, mandatory-profiles, hkcu, terminal-server, reference]
layer: reference
gedateerd: ja
bron: core-knowledge-docs
---

# Flex Profiles and PowerFuse profile storage (reference)

With mandatory profiles, HKCU settings are captured and persisted in a local file on disk rather than in a roaming profile: in **Flex Profiles** this is the OSP file; in **RES PowerFuse** it is stored in "User Preferences". Settings are written out on logoff and reloaded on logon.

For application virtualization (e.g. Citrix streamed apps), PowerFuse used **Generic Isolation Integration** via the PFGII.exe process, which made PowerFuse settings available inside the virtual application environment. It was enabled per streamed application in the management console.

Dated, product-specific reference.

*Bron: Core Knowledge doc 'TS, Mem Usage, Shadow Key and (Flex) Profile Core Doc' (Bas zijn vroege sysadmin-naslag).*

## Verwante notities

- [Hybrid user profiles vs roaming profiles](hybrid-user-profiles-explained.md)
- [PowerFuse application, file, and IP security (reference)](powerfuse-application-and-file-security.md)
- [PowerFuse Instant LogOff (reference)](powerfuse-instant-logoff.md)
- [Profile Portability: an abstraction layer over the user profile](profile-portability-abstraction-engine.md)
- [RES PowerFuse / Workspace Manager (reference)](res-powerfuse-workspace-manager-overview.md)
- [VAS Application Virtualization Delivery Flow](vas-application-virtualization-flow.md)
- [How a Windows user profile loads](windows-roaming-profile-loading.md)
