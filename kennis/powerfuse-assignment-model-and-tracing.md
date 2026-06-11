---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [res, powerfuse, assignment, powerzone, powertrace, reference]
layer: reference
gedateerd: ja
bron: core-knowledge-docs
---

# PowerFuse assignment model and tracing (reference)

PowerFuse decided what a user got based on three dimensions:

- **Powerzones** (determined by IP address range),
- **Workspace-containers** (based on computers / Terminal Servers),
- **security groups**.

An application could be assigned to everyone, or scoped by a Powerzone, a Workspace-container, or a security group. When scoped by more than one, the user had to satisfy all of them (AND logic), otherwise the application was not assigned.

Troubleshooting used **Workspace Analysis**: double-clicking a user opened a console showing every PowerFuse setting applying to that user, plus the **event log** depicting the whole login process and flagging failures. **PowerTrace** collected application/website usage and session/resource data for later analysis, viewable per application in the admin console or per user in the Workspace Analysis console.

Dated reference for how PowerFuse targeted and traced workspace configuration.

*Bron: Core Knowledge doc 'Powerfuse Core Doc' (Bas zijn vroege sysadmin-naslag).*

## Verwante notities

- [Citrix policy precedence: IMA vs Citrix AD vs normal AD policies](citrix-policy-precedence-ima-ad.md)
- [PowerFuse application, file, and IP security (reference)](powerfuse-application-and-file-security.md)
- [PowerFuse Instant LogOff (reference)](powerfuse-instant-logoff.md)
- [PowerFuse performance shields (reference)](powerfuse-performance-shields.md)
- [RES PowerFuse / Workspace Manager (reference)](res-powerfuse-workspace-manager-overview.md)
- [Terminal Server / Citrix troubleshooting checklist (own notes)](terminal-server-troubleshooting-checklist.md)
