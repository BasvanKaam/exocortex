---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [nerdio, avd, security, hardening, azure, method]
layer: reference
gedateerd: nee
bron: nerdio-content
---

# Hardening Nerdio and AVD: Easy Way vs Hard Way

Nerdio out of the box is not securely deployed. Bas frames hardening as two tiers, where the harder option is the better one:

- **Easy way**: enable the firewall on all relevant resources (storage accounts, key vaults).
- **Hard way (best)**: enable private endpoints so all traffic stays inside the customer's Azure environment.

Almost any resource in an Azure/AVD environment can be locked down:

- **Storage accounts**: firewall and private endpoints.
- **App service**: vNet integration with an internal subnet, accessible only from inside the Azure environment.
- **Key vaults**: firewall.

Key point he stresses: locking resources down does not cost anything, so it should always be advised (and help offered) to customers. Nerdio has standard documentation on how to harden a deployment.

*Bron: Nerdio-content 'CORE DOC... Hardening Nerdio and AVD' (Core Docs).*

## Verwante notities

- [Hardening a Nerdio Manager install (AVD)](avd-nerdio-manager-hardening-items.md)
- [AVD / NME outbound firewall allow-list](avd-nme-outbound-firewall-allowlist.md)
- [AVD Security cheat sheet v2.0 — 44 best practices](avd-security-cheat-sheet-v2.md)
- [Harden step by step and verify between steps, don't lock everything at once](harden-step-by-step-not-all-at-once.md)
- [Hardening the Nerdio Manager Console Itself](nerdio-manager-hardening-checklist.md)
- [NME Hardening: The Resource-by-Resource Sequence](nme-hardening-checklist-private-endpoints.md)
- [Hardening NME with private endpoints (the full approach)](nme-hardening-private-endpoints.md)
- [Hardening Nerdio Manager for MSP: the private-endpoint pattern](nmm-hardening-private-endpoint-pattern.md)
- [Nerdio Is Not Secure Out of the Box, So Always Harden](positie-nerdio-not-secure-out-of-the-box.md)
- [Server hardening can be easy — so there is no excuse](server-hardening-can-be-easy-no-excuse.md)
