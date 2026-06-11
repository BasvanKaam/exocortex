---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [citrix, xenapp, ica, reference, obsolete]
layer: reference
gedateerd: ja
bron: core-knowledge-docs
---

# Citrix XenApp Lineage and Client Types

Citrix XenApp is the former MetaFrame and Presentation Server. RDP has been licensed from Citrix's ICA since 1997. XenApp does application virtualization: it streams apps to the desktop, runs them in an isolated environment, and uses caching so apps stay available when offline. XenApp includes Citrix Secure Gateway and the web-based client.

Client/plug-in types:
- **Online plug-in (PN Agent)**: the renamed client for server-side virtualization (published applications). The PN Agent uses the web interface for central configuration without opening IE; app icons can be published to the Start menu, system tray, and desktop. Nothing needs user configuration.
- **PN Full**: locally installed, largely configured by the user/admin on site, uses custom connections; specific changes go in the .INI file.
- **Offline plug-in (Streaming Client)**: for client-side application virtualization (application streaming).
- **Web client**: same capabilities as the PN Agent but via a web interface, so no client is needed; all configuration is central.

*Bron: Core Knowledge doc 'Citrix General Core Doc' (Bas zijn vroege sysadmin-naslag).*

## Verwante notities

- [Citrix company history: from Citrus to WinFrame](citrix-company-history.md)
- [Citrix IMA Architecture: Data Store and Local Host Cache](citrix-ima-architecture.md)
- [Citrix origins: from Citrus Systems to WinFrame, and the birth of ICA](citrix-origins-and-ica-birth.md)
- [Citrix Receiver: purpose and naming history](citrix-receiver-history-and-purpose.md)
- [Citrix Streaming Profile and AIE Data Paths](citrix-streaming-profile-paths.md)
- [The origin of Citrix and the ICA protocol](history-of-citrix-and-ica.md)
