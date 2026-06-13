---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [nme, hardening, private-endpoints, azure, security, avd]
layer: reference
gedateerd: ja
bron: nerdio-training
---

# Hardening NME with private endpoints (the full approach)

NME ships optimised for functionality and accessibility, not security. Hardening is what aligns it to CIS, NIST and ISO 27001, shrinks the attack surface and gives operational resilience.

## Why hardening is a post-installation / post-sales task
- App Service, SQL and Key Vault need **public access during deployment** to pull resources. Enforce private endpoints too early and the services can't connect, so deployment fails.
- A **private endpoint can't be created for a resource that doesn't exist yet**. SQL, Storage, Key Vault and Automation Accounts must be deployed first, then locked down.
- **Private DNS zones must be linked to existing resources**, so DNS comes after deployment.
- Hardening is **iterative and verified at each stage**: lock down, test connectivity, repeat. Lock everything at once and you can't tell what broke.
- It's customer-specific (policies, compliance frameworks, networking, multiple sign-off teams), so it commonly takes longer than the 30-day trial and lands in the post-sales / paid PoV phase.

## Core concepts
- **vNet**: foundation for all private networking; keeps NME-to-service traffic on Azure's private backbone instead of the public internet. Two isolated subnets: one for private endpoints (`nme-endpoints-subnet`), one for the App Service (`nme-app-subnet`).
- **Private Endpoint**: assigns a private IP from a vNet subnet to an Azure service (SQL, Storage, Key Vault, App Service, Automation). Traffic stays on Microsoft's backbone; lower latency; removes need for VPN/ExpressRoute/public allow-lists.
- **Private DNS Zone**: maps the service's public FQDN (e.g. `database.windows.net`) to the private IP. Without it, resources inside the vNet still resolve to the public endpoint and the whole point is lost.
- **Private Endpoint vs Service Endpoint**: a private endpoint gives a private IP and fully isolates the service (best for high-security). A service endpoint gives no private IP; it trusts traffic from a specific vNet while still using the public endpoint (fine when public access is acceptable but should be network-restricted).

## Private DNS zones you need
- Key Vault: `privatelink.vaultcore.azure.net`
- SQL: `privatelink.database.windows.net`
- Automation: `privatelink.azure-automation.net`
- Storage (blob): `privatelink.blob.core.windows.net` (and `privatelink.file.core.windows.net` for FSLogix files)
- App Service: `privatelink.azurewebsites.net`
- Optional Azure Monitor: `privatelink.monitor.azure.com`, `privatelink.oms.opinsights.azure.com`, `privatelink.ods.opinsights.azure.com`, `privatelink.agentsvc.azure-automation.net` (caution: Monitor uses shared public endpoints, can impact Log Analytics across services).

## Manual step order (each step verifiable in between)
1. Create the private vNet + two subnets (suggested CIDRs: vNet /23, endpoints subnet /24, app subnet /28; disable Private Endpoint Network Policies on the endpoint subnet).
2. Create and link the private DNS zones to the vNet.
3-7. Create private endpoints for Key Vaults (app + cost-calculator), SQL (`sqlServer` sub-resource), Automation Account (`DSCAndHybridWorker`), Storage Accounts (DPS, CCL, FSLogix; `blob`), and the App Services (Nerdio + CCL; `sites`).
8. Enable vNet Integration for the App Services (to `nme-app-subnet`) and explicitly set Public Network Access = Disabled.
9-11. Disable public access on Key Vaults (keep "allow trusted Microsoft services" checked), SQL, and Storage Accounts.
12. Optionally peer additional vNets (e.g. the AVD vNet), then restart the App Service (mandatory to apply changes).
13-14. Optionally make the Scripted Actions Automation + Storage (CSSA) private and deploy a Hybrid Worker VM.

## Naming and gotchas
- All NME backend services are **Azure PaaS** (cloud-native); the "SQL server" name is misleading.
- The **Scripted Actions storage account (CSSA) is not created on install**; you must first run a Scripted Action (e.g. the Nerdio update action) to trigger it.
- If you enable "Restrict App Service public access", NME is unreachable after deploy until you add a way in (proxy/jump box in the same vNet, vNet peering, or VPN). Build the proxy machine early; it takes time.
- After locking SQL/Storage/Key Vault, disabling public access does not affect private-endpoint / vNet access; trusted Microsoft services can still reach them when allowed.
- **Disable FTP** on the App Service (Configuration > General Settings > FTP State = Disabled): not needed by NME, removes a credential-attack surface. Also use NSGs to control outbound traffic and trim unnecessary diagnostic logs.

## Automated install hardening (as of NME 7.2.0 / GUI tab in 7.3)
You can configure private endpoints for the App Service during installation, with optional "restrict App Service public access". Fast, consistent, secure baseline, but limited to what the wizard exposes (no fine-grained DNS, custom subnetting or peering). Recommended hybrid approach: enable private endpoints at install if your network/DNS already support them, then add manual scripted-action hardening for storage, monitoring and advanced DNS.

*Bron: Nerdio-content 'Hardening Nerdio Manager for Enterprise Services v1.0' (Training).*

## Verwante notities

- [Hardening a Nerdio Manager install (AVD)](avd-nerdio-manager-hardening-items.md)
- [AVD Security cheat sheet v2.0 — 44 best practices](avd-security-cheat-sheet-v2.md)
- [Hardening Nerdio and AVD: Easy Way vs Hard Way](hardening-nerdio-avd-easy-vs-hard.md)
- [Hardening the Nerdio Manager Console Itself](nerdio-manager-hardening-checklist.md)
- [Hardening Nerdio Manager for MSP: the private-endpoint pattern](nmm-hardening-private-endpoint-pattern.md)
- [Nerdio Is Not Secure Out of the Box, So Always Harden](positie-nerdio-not-secure-out-of-the-box.md)
