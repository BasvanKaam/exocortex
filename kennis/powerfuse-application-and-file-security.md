---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [res, powerfuse, security, whitelisting, reference]
layer: reference
gedateerd: ja
bron: core-knowledge-docs
---

# PowerFuse application, file, and IP security (reference)

PowerFuse enforced workspace security through several whitelisting modules:

- **Application security**: any application reachable by the user was automatically authorized; everything else was blocked unless listed under "globally authorized files". Because applications often launch other applications (e.g. winhlp32.exe), you authorized at application level or added the helper explicitly.
- **Files and folders**: first define protected file types or folders (e.g. *.vbs, *.mp3), then authorize specific access at application level or globally.
- **Read-only blanketing**: made all local drives read-only for users, then granted write access only where needed.
- **Removable drives**: assigned read/write rights per user and location for floppy, CD/DVD, and USB/FireWire devices to stop data exfiltration.
- **IP connections**: blocked unauthorized applications from opening IP connections; many apps (databases, ICA/RDP clients, telnet, messengers) open their own connections and had to be authorized per application.

Dated reference for how RES PowerFuse locked down a Terminal Server workspace.

*Bron: Core Knowledge doc 'Powerfuse Core Doc' (Bas zijn vroege sysadmin-naslag).*

## Verwante notities

- [Flex Profiles and PowerFuse profile storage (reference)](flex-profiles-powerfuse-profile-storage.md)
- [PowerFuse assignment model and tracing (reference)](powerfuse-assignment-model-and-tracing.md)
- [PowerFuse Instant LogOff (reference)](powerfuse-instant-logoff.md)
- [PowerFuse performance shields (reference)](powerfuse-performance-shields.md)
- [RES PowerFuse / Workspace Manager (reference)](res-powerfuse-workspace-manager-overview.md)
- [Rights vs permissions are not the same thing](rights-vs-permissions-windows.md)
- [Share vs NTFS Permissions](share-vs-ntfs-permissions.md)
