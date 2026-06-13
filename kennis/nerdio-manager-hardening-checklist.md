---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [nerdio, security, hardening, rbac, scripted-actions, cheat-sheet]
layer: reference
gedateerd: ja
bron: nerdio-blog
---

# Hardening the Nerdio Manager Console Itself

When securing AVD with Nerdio, don't forget to add Nerdio to the shared-responsibility map and harden the management plane itself.

- **Role-Based Access**: custom roles following least privilege.
- **Scripted Actions**: use the secure vault and secure variables for secrets.
- **Harden the Nerdio Manager deployment**: harden and replicate the SQL database, harden the storage account and app service, configure backup/restore and BCDR, put an Application Gateway + Web Application Firewall in front.
- **Enable conditional access** to the Nerdio console.
- **Remove FTP services** from the Nerdio App Service.
- Logging is collected/enabled automatically by Nerdio.

General starting points beyond the tool: Microsoft Secure Score, user security-awareness training.

*Bron: Nerdio-content 'Nerdio - AVD security cheat sheet' (Blogs).*

## Verwante notities

- [Hardening a Nerdio Manager install (AVD)](avd-nerdio-manager-hardening-items.md)
- [AVD Security Checklist by Layer (Bas's Cheat Sheet)](avd-security-checklist-by-layer.md)
- [AVD Shared Responsibility: Who Secures What](avd-shared-responsibility-model.md)
- [Hardening Nerdio and AVD: Easy Way vs Hard Way](hardening-nerdio-avd-easy-vs-hard.md)
- [Permissions to Install and Operate Nerdio (NME)](nerdio-install-and-linking-permissions.md)
- [Hardening NME with private endpoints (the full approach)](nme-hardening-private-endpoints.md)
- [NME first-admin RBAC and log analytics retention savings](nme-rbac-first-admin-and-savings.md)
- [NME / AVD troubleshooting cheat sheet](nme-troubleshooting-cheatsheet.md)
- [Nerdio Is Not Secure Out of the Box, So Always Harden](positie-nerdio-not-secure-out-of-the-box.md)
- [Zero Trust extras: patching cadence and CIS-hardened images](zero-trust-hardening-extras-patch-cis-images.md)
