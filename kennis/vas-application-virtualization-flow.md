---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [application-virtualization, active-directory, reference, vas]
layer: reference
gedateerd: ja
bron: core-knowledge-docs
---

# VAS Application Virtualization Delivery Flow

Reference note on how the VAS server delivered virtualized applications.

Components:
- The VAS server holds the application packages.
- A datastore holds the application information, written to a backing datastore database.
- The management console makes changes to application configurations and talks to the management web service on the VAS server, which writes those changes into the datastore.

Delivery flow at logon:
1. User logs on at the workstation and authenticates against Active Directory.
2. Credentials plus group memberships are passed to the VAS server.
3. The VAS server compares those groups against the applications registered in the datastore.
4. Matching applications are placed on the desktop, start menu and similar.
5. A small leading portion of the application is loaded from the VAS server so it can start; the user begins working while the rest streams down in the background.

*Bron: Core Knowledge doc 'VAS Basic Core Doc' (Bas zijn vroege sysadmin-naslag).*

## Verwante notities

- [Application virtualisation tops out around 70-80% in practice](app-virtualisation-ceiling-70-80.md)
- [Application layering complements, does not replace, app virtualization](application-layering-vs-virtualization.md)
- [Citrix Streaming Profile and AIE Data Paths](citrix-streaming-profile-paths.md)
- [Flex Profiles and PowerFuse profile storage (reference)](flex-profiles-powerfuse-profile-storage.md)
- [Microsoft App-V components and licensing with Citrix](microsoft-app-v-with-citrix.md)
- [RES PowerFuse / Workspace Manager (reference)](res-powerfuse-workspace-manager-overview.md)
