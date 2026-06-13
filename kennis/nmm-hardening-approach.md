---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [nmm, msp, hardening, azure, security, app-service, sql]
layer: reference
gedateerd: ja
bron: nerdio-training
---

# Hardening NMM (MSP) – the supported approach (differs from NME)

Key correction: **NMM is not hardened the same way as NME.** NMM has **no "Enable Private Endpoints" runbook**, and the NMM docs do **not** prescribe creating private endpoints / private DNS zones for App Service, SQL, Key Vault or Automation. There's also no automated install-time hardening wizard and no NMM "pre-flight script." All NMM hardening is post-install.

## The actual NMM hardening surface
1. **App Service Access Restrictions** (NMM's entry point). By default the App Service is Entra-ID protected but reachable from anywhere. Allow-list admin IP ranges (or your gateway's IP) under Networking > Access restrictions; an automatic Deny All rule blocks everything else.
2. **Azure SQL hardening, two supported patterns:**
   - **Option A – Outbound IP allow-list**: add the App Service outbound IPs to the SQL firewall; keep `Allow Azure services = Yes`, `Deny public network access = No`. Simpler, but IPs can change on service moves.
   - **Option B (recommended) – VNet Integration + SQL service endpoint**: enable App Service VNet Integration to a delegated /28+ subnet (delegated to `Microsoft.Web`), add an Azure SQL service endpoint for that vNet, then set `Allow Azure services = No` and `Deny public network access = Yes`. Routes App Service→SQL privately via your vNet, avoiding shared outbound IPs.
   - Note NMM uses a **service endpoint** here, not a private endpoint.
3. **VNet Integration plan requirement**: needs a /28-or-larger subnet delegated to Microsoft.Web. Some Basic SKUs now support it; otherwise upgrade to Premium (P2v3/P3v3).
4. **(Optional) NAT Gateway** for controlled egress: integrate the App Service with a vNet backed by a NAT Gateway to present a fixed outbound public IP for third-party allow-lists.
5. **(Optional) Application Gateway + WAF** fronting: place an App Gateway with WAF in front of NMM, attach custom domain/cert, point DNS at the gateway, then restrict direct App Service access to the gateway's IP(s) via Access Restrictions.
6. **Health check**: enable the NMM REST API (Partner API), then hit `https://<nmm-url>/healthStatus` (rate-limited to 1 request / 5 min) to verify SQL/Azure/AVD connectivity from the App Service; use Application Insights to diagnose failures.
7. **FTP/FTPS**: recent NMM releases disable FTPS by default on the App Service; verify and keep disabled unless required.

## Backup / restore in hardened NMM (2025 guidance)
- App Service: Azure hourly automatic backups; custom backups can include the linked DB (note DB size limits).
- SQL: Azure automated backups, adjust retention.
- Key Vault: use Nerdio's PowerShell script for a one-time export of keys/secrets/certs.
- **Hardened-SQL caveat**: App Service **custom backups run from the App Service cluster, not over VNet/PE**, so if you've denied public SQL access you must still allow the App Service cluster IPs on the SQL firewall for custom backups to work.

## Storage caveat
Don't blindly make AVD-profile storage private-endpoint-only: features like Azure Files autoscale and handle lookups may need extra allowances and can break. If you lock down storage, review the relevant troubleshooting guidance first.

*Bron: Nerdio-content 'hardening_nmm_lesson' (Training).*

## Verwante notities

- [Hardening Nerdio Manager for MSP: the private-endpoint pattern](nmm-hardening-private-endpoint-pattern.md)
