---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-11
tags: [euc, daas, comparison, wvd, fslogix, azure]
layer: reference
gedateerd: ja
bron: cgit
---

# EUC alternatives feature comparison (CloudJumper, Workspot, Parallels)

Feature matrix used to compare three Citrix alternatives in 2019. Axes that mattered:

- **Supported IdPs:** classic AD, Azure AD, ADDS, SAMLv2.0 (Workspot/CloudJumper); Parallels lacks ADDS.
- **FMA and SSO:** all yes.
- **Auto install and config:** CloudJumper/Workspot yes; Parallels partial.
- **Protocol:** all RDP.
- **Image management:** all yes.
- **Document management:** only CloudJumper (OneDrive, Azure Files).
- **Power and scaling options:** CloudJumper/Workspot yes; Parallels coming soon.
- **On-premises deployment:** only Parallels.
- **Profile management:** all UPD/FSLogix.
- **Multi-tenant:** CloudJumper/Workspot yes; Parallels coming soon.
- **HTML5 web portal:** all yes.
- **Control plane location:** CloudJumper Azure; Workspot Azure/AWS (US); Parallels Azure (coming) or on-prem.

Takeaway dimensions: where the control plane lives, how complete the automation is, and whether on-prem is supported.

*Bron: Salomon-IT '5 alternatieven' (CGIT Event).*

## Verwante notities

- [The cheat-sheet method: one A4 to compare a crowded field](cheat-sheet-comparison-method.md)
- [Session proposition: five (cloud) alternatives to Citrix and VMware](five-cloud-alternatives-to-citrix-vmware-session.md)
- [Baseline Criteria for Modern App and Desktop Delivery (anno 2020)](modern-workplace-delivery-baseline-2020.md)
- [Workspot's cloud-born portfolio: Desktop/Workstation/App/DR Cloud](workspot-four-product-portfolio.md)
