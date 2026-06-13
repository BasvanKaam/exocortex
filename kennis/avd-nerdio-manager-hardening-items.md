---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [nerdio, avd, security, hardening, private-link]
layer: reference
gedateerd: ja
bron: nerdio-blog
---

# Hardening a Nerdio Manager install (AVD)

Nerdio-specific hardening steps for the Nerdio Manager PaaS install, distinct from generic AVD security:

- **Harden the SQL service.** App-to-DB and data-at-rest are encrypted by default. Further harden by adding the app service outbound IP to the SQL firewall (only your Nerdio Manager IPs reach the server) and routing traffic via a vNet with an Azure SQL service endpoint.
- **Harden the storage account.** Storage accounts hold FSLogix profiles, boot diagnostics, scripted actions, and MSIX app attach packages. Tighten with Private Link.
- **Harden the app service.** The App Service is the entry point; protected by Entra auth + MFA + conditional access by default but reachable from any internet location. Lock down with Access Restrictions or a Private Endpoint / Private Link; remove the FTP service.
- **App gateway + web app firewall.** Front the manager with a new URL/domain pointed at the gateway, a PFX SSL cert whose CN matches that domain; decide public vs Azure-network-restricted.
- **RBAC** with least-privilege; custom roles optional.
- **Scripted Actions** are PowerShell run in a Windows VM or Azure Automation Account; pass sensitive values via Global Secure Variables stored in Azure Key Vault and referenced as `$SecureVars.Variable_Name`.
- **Logging** is on by default in Nerdio, accessible from the console, distinguishes automated (e.g. autoscale) vs manual actions with timestamps, and can pull VM logs for troubleshooting.

**Private Link is the headline recommendation.** Bas recommends Private Link (with Private Endpoints) for the Nerdio install, specifically the App Services, Key Vaults, and Storage Accounts, so communication stays local to the vNet and the service is no longer publicly available. Private Link is often a security prerequisite for a company to be allowed to use Nerdio at all. It is configurable only on Azure PaaS services, not on AVD hosts. When troubleshooting, check DNS and firewall (service and network). Note the distinction he stresses: Private Link vs Private Endpoint are related but configured separately; and a Service Endpoint stays a publicly routable IP, so he prefers Private Endpoints.

*Bron: Nerdio-content 'Azure Virtual Desktop Security Guidelines Cheat Sheet - v2.0' (Blogs).*

## Verwante notities

- [AVD security cheat sheet: the six-category framework](avd-security-cheat-sheet-framework.md)
- [Hardening Nerdio and AVD: Easy Way vs Hard Way](hardening-nerdio-avd-easy-vs-hard.md)
- [Hardening the Nerdio Manager Console Itself](nerdio-manager-hardening-checklist.md)
- [NME Hardening: The Resource-by-Resource Sequence](nme-hardening-checklist-private-endpoints.md)
- [Hardening NME with private endpoints (the full approach)](nme-hardening-private-endpoints.md)
- [Nerdio Is Not Secure Out of the Box, So Always Harden](positie-nerdio-not-secure-out-of-the-box.md)
