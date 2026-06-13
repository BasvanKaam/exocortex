---
type: positie
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [positie, permissions, nerdio, security]
bron: nerdio-content
---

# Always Test Before Revoking API Permissions

Bas's stance: when a customer's security team wants to revoke certain Nerdio API permissions, do not assume it is safe. It is not always clear what will break or what errors NME will surface when a given permission is removed. Testing is mandatory for any API permission change, and when unsure, consult colleagues or NME support / product management rather than guessing. This sits alongside his general view that read and delegated permissions are an easy sell, while write/write.all and broad application permissions are where customer security friction concentrates, so the field should expect and plan for that pushback.

*Bron: Nerdio-content 'CORE DOC... Permissions' (Core Docs).*

## Verwante notities

- [Delegated vs Application Permissions (Microsoft Graph)](delegated-vs-application-permissions-graph.md)
- [Harden step by step and verify between steps, don't lock everything at once](harden-step-by-step-not-all-at-once.md)
- [Permissions to Install and Operate Nerdio (NME)](nerdio-install-and-linking-permissions.md)
- [NME / AVD troubleshooting cheat sheet](nme-troubleshooting-cheatsheet.md)
- [Only the Documented, Supported API Counts; Internal APIs Are Out of Bounds](position-only-document-the-supported-public-api.md)
- [Why Windows 365 enablement needs Global Admin (org consent)](windows-365-enablement-permissions.md)
