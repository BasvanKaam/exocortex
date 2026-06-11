---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [res, powerfuse, profiles, logoff, terminal-server, reference]
layer: reference
gedateerd: ja
bron: core-knowledge-docs
---

# PowerFuse Instant LogOff (reference)

Instant LogOff dealt with user profiles that failed to release because some applications kept registry handles open. On logoff it enumerated all handles to the user registry and force-closed any that did not close automatically. It ran in "log only" mode to detect problems or "enabled" to act on them.

It could also tear down the user session immediately on logoff, which improved perceived speed and suppressed the "your settings are being saved" screen that appeared unexpectedly with seamless-windows applications.

Dated reference for a recurring Terminal Server profile-release pain point.

*Bron: Core Knowledge doc 'Powerfuse Core Doc' (Bas zijn vroege sysadmin-naslag).*

## Verwante notities

- [Flex Profiles and PowerFuse profile storage (reference)](flex-profiles-powerfuse-profile-storage.md)
- [Last write wins: why roaming profiles collide across sessions](last-write-wins-ntuser-dat.md)
- [PowerFuse application, file, and IP security (reference)](powerfuse-application-and-file-security.md)
- [PowerFuse assignment model and tracing (reference)](powerfuse-assignment-model-and-tracing.md)
- [PowerFuse performance shields (reference)](powerfuse-performance-shields.md)
- [RES PowerFuse / Workspace Manager (reference)](res-powerfuse-workspace-manager-overview.md)
- [How a Windows user profile loads](windows-roaming-profile-loading.md)
