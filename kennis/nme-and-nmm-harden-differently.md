---
type: positie
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [nme, nmm, hardening, positie, security]
bron: nerdio-training
---

# NME and NMM are hardened differently; don't copy one onto the other

A correction I made explicit after an earlier draft got it wrong: the NME hardening playbook (private endpoints, private DNS zones, an "Enable Private Endpoints" runbook, a Hybrid Worker VM for scripted actions, automated install-time hardening) does **not** apply to NMM. None of that is in the NMM documentation. NMM's supported path is App Service Access Restrictions plus SQL hardening (outbound-IP allow-list, or VNet Integration + SQL service endpoint), with optional NAT Gateway for egress and Application Gateway + WAF fronting.

My stance: verify against the actual product docs (nmmhelp.getnerdio.com) per product, never assume the two managers harden the same way, and never recommend a control the product doesn't actually support. Locking down storage to private-endpoint-only can also break AVD profile features (Azure Files autoscale, handle lookups), so that's not a free win either.

*Bron: Nerdio-content 'hardening_nmm_lesson' (Training).*

## Verwante notities

- [NME to NMM migration runbook (AVD)](nme-to-nmm-migration-runbook.md)
- [Hardening Nerdio Manager for MSP: the private-endpoint pattern](nmm-hardening-private-endpoint-pattern.md)
