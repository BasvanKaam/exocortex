---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [nerdio, nmm, msp, azure, hardening, security, sql, app-service]
layer: reference
gedateerd: ja
bron: nerdio-training
---

# NMM Hardening: Why It Uses Service Endpoints and Access Restrictions, Not Private Endpoints

A key architectural distinction Bas draws: Nerdio Manager for MSP (NMM) hardens differently from NME. By design NMM uses **App Service Access Restrictions** plus **VNet Integration with Service Endpoints**, instead of the Private Endpoint / Private DNS model used for NME. The default deployment is public-endpoint, no PE/Private DNS by design, prioritizing flexibility and PoC speed.

The NMM hardening sequence:

1. **Pre-flight**: validate subscription permissions, check provider registrations (Microsoft.Web, Microsoft.Sql, etc.), locate deployed resources (App Service, SQL, Key Vault), document baseline.
2. **App Service Access Restrictions**: allow rules for trusted IPs/gateways, then a default deny for everything else.
3. **SQL hardening, two supported methods:**
   - Option A: outbound IP allow-listing on the SQL firewall (document the App Service outbound IPs, add firewall rules).
   - Option B (recommended): App Service VNet Integration with a SQL service endpoint, with SQL public network access disabled.
4. **VNet Integration requirements**: delegated subnet, and an App Service plan tier upgrade if required.
5. **Optional egress control**: NAT Gateway to centralize/control egress and provide a static outbound IP when third-party allow-lists need one.
6. **Optional front-end security**: Application Gateway + WAF in front of NMM, with a custom domain/cert, and direct App Service access restricted to force the WAF path.
7. **Verify /health Status endpoint** (requires the NMM REST API enabled).
8. **Backup & restore** per updated 2025 guidance for App Service, SQL, and Key Vault, accounting for firewall rules in a hardened setup.
9. **Confirm FTPS** is disabled (default in recent releases).
10. **AVD session host outbound access**: ensure documented URLs/ports are allowed via NSG/firewall.

A useful teaching artifact he calls for: a decision chart of Outbound IPs vs. VNet Integration for SQL.

Version-specific; recheck against current NMM release.

*Bron: Nerdio-content 'ADDIE - Hardening Nerdio Manager for MSP' (Training).*

## Verwante notities

- [Hardening Nerdio Manager for MSP: the private-endpoint pattern](nmm-hardening-private-endpoint-pattern.md)
