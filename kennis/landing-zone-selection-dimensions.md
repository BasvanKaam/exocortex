---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-11
tags: [landing-zone, decision-tree, placement, cloud-strategy, enterprise-architecture]
layer: reference
gedateerd: nee
attributie: weolcan-wcgf
bron: salomon-cloud-governance
---

# Landing zone selection dimensions and the decision tree

> Referentie uit het Weolcan Cloud Governance Framework (WCGF). Niet Bas zijn eigen IP, hier bewaard als naslag.

Beyond the SaaS/PaaS/IaaS preference, a real Cloud Strategy is more fine-grained and offers multiple target landing zones. Example dimensions that drive a workload toward a specific landing zone:

- Applications relying on traditional database platforms may need a separate landing zone compatible with the licensing model.
- Data classified as 'secret' may require additional security.
- Functionality dependent on traditional ERP applications may require close proximity.
- Some functionality may be developed on low-code / no-code platforms.

Determining decision criteria and rules upfront is challenging but lets both the business and the enterprise architects follow the same rules, providing clarity about the sourcing strategy. The recommended way to represent these decision rules is a decision tree.

*Bron: Salomon-IT 'Cloud Strategy - Cloud Governance'.*

## Verwante notities

- [Cloud Placement Decisions: the application lifecycle quadrant](cloud-placement-decisions-quadrant.md)
- [What makes a good Cloud Strategy](cloud-strategy-quality-criteria.md)
