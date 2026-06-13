---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [nerdio, nme, zero-trust, security, euc, architecture]
layer: reference
gedateerd: nee
bron: nerdio-training
---

# Mapping Zero Trust Principles to Real NME Capabilities

Bas's framework for teaching Zero Trust in an EUC/DaaS context: don't teach Zero Trust abstractly, map each principle to a concrete, available product capability. The pairing:

- **Verify explicitly / least privilege** -> Entra ID integration and auth model, MFA/Conditional Access context, Nerdio role-based access control, separation of duties, subscription linking and permission boundaries, managed identity vs app registration.
- **Assume breach** -> network isolation, private endpoints, VNet integration; securing SQL, Key Vault, Storage, Automation Account; reducing public exposure.
- **Reduce blast radius / supply-chain risk** -> scripted actions as a security boundary, global secure variables + Key Vault, automation account managed identity, script signing, approval models.
- **Device trust** -> Intune integration, security baselines / CIS alignment, policy backup-compare-restore to catch configuration drift.
- **Continuous validation** -> audit logging, log shipping + Application Insights, exception logs, alerts, Azure Monitor / AVD Insights, incident detection flow.
- **Compliance & governance** -> privacy model, PII detection, evidence collection, alignment to CIS/NIST/ISO.
- **Day-two operations** -> secure remote support, Console Connect access control, onboarding/offboarding, break-glass access, periodic review.

Two conceptual distinctions he teaches up front and returns to:
1. **Control plane vs workload plane** security (where Nerdio Manager operates vs where customer workloads run).
2. The **shared responsibility model** between Microsoft, Nerdio, and the customer.

This mapping pattern (principle -> available feature) is reusable for any "map a framework onto a product" training.

*Bron: Nerdio-content 'ADDIE - Map Zero Trust Model to NME' (Training).*

## Verwante notities

- [Zero Trust Identity Controls in Nerdio (AVD + W365)](zero-trust-controls-nerdio-avd-w365.md)
- [Zero Trust principles mapped to AVD and Windows 365 in NME](zero-trust-mapped-to-avd-w365-nme.md)
