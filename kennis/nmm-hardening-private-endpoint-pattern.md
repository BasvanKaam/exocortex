---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [nerdio, nmm, msp, security, hardening, azure, private-endpoint, networking]
layer: reference
gedateerd: ja
bron: nerdio-training
---

# Hardening Nerdio Manager for MSP: the private-endpoint pattern

NMM runs inside your own tenant/subscription and uses App Service (the portal), Azure SQL, Key Vault, Storage, and Automation. A default install is reachable from the public internet. The goal of hardening is to isolate the management plane and data plane from the internet, enforce least-privilege networking, and disable nonessential surface, while preserving full AVD and NMM automation functionality. Verify each control against the current NMM Help Center / Microsoft Learn before applying; specifics drift.

## The components to harden (control mapping)
- App Service (NMM portal): VNet Integration; Access Restrictions or Private Endpoint; HTTPS-only and TLS >= 1.2; disable FTP/FTPS where possible.
- Azure SQL (NMM DB): Private Endpoint (preferred) or service endpoint; set Public network access = Disabled on the logical server.
- Key Vault (NMM secrets): Private Endpoint; disable public access.
- Storage (scripts/artifacts): Selected networks, or Public network access = Disabled plus Private Endpoints for blob/file; disallow anonymous blob access.
- Automation: Private Endpoints; add a Hybrid Runbook Worker if you fully privatize the storage/script paths.
- Networking: Private DNS zones; optional NAT Gateway for stable egress; optional Application Gateway + WAF for controlled publishing.

## The ordered hardening flow
VNet Integration -> Private DNS -> Private Endpoints (SQL, Key Vault, Storage, Automation) -> App Service inbound controls -> optional Hybrid Worker -> confirm outbound allowances.

1. Pre-flight: inventory all NMM resources; plan NAT and VNet topology; announce a maintenance window.
2. Enable VNet Integration for the App Service. Tier matters (Premium v3 is often required); the subnet must be delegated to Microsoft.Web and be /28 or larger.
3. Provision Private DNS zones and link them to the VNet(s): privatelink.azurewebsites.net (include the <app>.scm host for Kudu/SCM), privatelink.database.windows.net, privatelink.vaultcore.azure.net, privatelink.blob.core.windows.net, privatelink.file.core.windows.net.
4. Harden Azure SQL: create a Private Endpoint on the logical server, then set Public network access = Disabled once the PE is healthy. Test from the VNet.
5. Harden Key Vault: add a Private Endpoint, disable public access, validate name resolution to the private IP from a VM in the VNet.
6. Harden Storage: Selected networks or Public network access = Disabled plus blob/file Private Endpoints; disallow anonymous blob access. Test read/write from the VNet.
7. Harden Automation: add Private Endpoints. If runbooks must reach storage you've made private, deploy a Hybrid Runbook Worker on a VM in the VNet and target it for scripted actions.
8. Harden the App Service inbound: start with Access Restrictions (allow corp/VPN/Azure Firewall egress, default deny); optionally add a Private Endpoint for the site (with DNS for the scm host); enforce HTTPS-only, TLS >= 1.2, disable FTP/FTPS.
9. Optional publishing layer: if the portal can't stay fully private, front it with Application Gateway + WAF (custom domain + cert mapped to NMM, WAF rules to the private site).
10. Outbound: keep HTTPS 443 open to the Microsoft/Azure control planes, Entra, and the AVD service endpoints required by NMM-managed session hosts.

## Verification
- SQL/Key Vault/Storage: confirm public access disabled, PEs healthy, connections succeed only via private link, blob anonymous access disabled.
- App Service: name resolves to a private IP in privatelink.azurewebsites.net, or Access Restrictions are in effect.
- Functional: sign in from an allowed path; run a Scripted Action against a test VM and confirm artifacts resolve over private endpoints (no public calls); validate AVD lifecycle actions and required session-host outbound still succeed.

## Day-2 rule of thumb
Whenever an NMM update or new feature introduces new resources (extra storage, diagnostics), repeat the same pattern: Private Endpoint + Private DNS + 'public off.'

Reference principle Bas applies when sourcing: cite NMM Help Center for NMM-specific controls, and only fall back to Microsoft Learn where NMM defers to Azure's native configuration (Key Vault / Storage / Automation private-endpoint details).

*Bron: Nerdio-content 'NMM hardening' (Training).*

## Verwante notities

- [Hardening Nerdio and AVD: Easy Way vs Hard Way](hardening-nerdio-avd-easy-vs-hard.md)
- [NME and NMM are hardened differently; don't copy one onto the other](nme-and-nmm-harden-differently.md)
- [NME Hardening: The Resource-by-Resource Sequence](nme-hardening-checklist-private-endpoints.md)
- [Hardening NME with private endpoints (the full approach)](nme-hardening-private-endpoints.md)
- [NMM architecture: native Azure PaaS deployed into the MSP's own tenant](nmm-architecture-paas-in-msp-tenant.md)
- [Hardening NMM (MSP) – the supported approach (differs from NME)](nmm-hardening-approach.md)
- [NMM Hardening: Why It Uses Service Endpoints and Access Restrictions, Not Private Endpoints](nmm-hardening-service-endpoints-vs-private-endpoints.md)
- [NMM's Un-Hardened Default Is a Deliberate Flexibility Choice](position-nmm-default-unhardened-is-deliberate.md)
