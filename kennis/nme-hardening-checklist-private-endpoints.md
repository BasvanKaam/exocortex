---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [nerdio, nme, azure, hardening, security, private-endpoints]
layer: reference
gedateerd: ja
bron: nerdio-training
---

# NME Hardening: The Resource-by-Resource Sequence

Nerdio Manager for Enterprise is not hardened out of the box by design (deployment prioritizes a working install); securing it is a deliberate post-install activity, increasingly demanded pre-sales to satisfy CIS, NIST, and ISO 27001.

The ordered hardening sequence Bas teaches, all verified step by step:

1. **Pre-flight**: run the Nerdio post-installation script to proactively surface any services that might block a successful install, and identify which ones.
2. **VNet Integration** for the Nerdio Manager App Service (secure local-only communication between the App Service and other Azure resources).
3. **Private DNS zones** set up to support the private endpoints.
4. Create **private endpoints** and restrict public access, resource by resource: Automation Account, the main App Service, the CCL App Service, Azure SQL Database, Azure Key Vault, Storage Accounts.
5. **Optional**: make the Scripted Actions automation and storage account (CSSA) private.
6. **Disable unnecessary services** to reduce attack surface (e.g. FTP on the App Service).
7. **Outbound firewall ports and URLs**: ensure AVD prerequisites (which apply even without Nerdio) plus VNet-integration ports/URLs are open on the firewall / NSG / whatever sits in between, so services communicate.

NME ships an "Enable Private Endpoint" runbook that can drive parts of this.

Note: version/product-specific; revisit against the current NME release and the announced new look and feel.

*Bron: Nerdio-content 'ADDIE - Hardening Nerdio Manager for Enterprise' (Training).*

## Verwante notities

- [Hardening a Nerdio Manager install (AVD)](avd-nerdio-manager-hardening-items.md)
- [Hardening Nerdio and AVD: Easy Way vs Hard Way](hardening-nerdio-avd-easy-vs-hard.md)
- [Hardening Nerdio Manager for MSP: the private-endpoint pattern](nmm-hardening-private-endpoint-pattern.md)
