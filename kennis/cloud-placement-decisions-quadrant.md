---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-11
tags: [cloud-governance, cloud-placement, application-lifecycle, quadrant-model, wcgf]
layer: reference
gedateerd: nee
attributie: weolcan-wcgf
bron: salomon-cloud-governance
---

# Cloud Placement Decisions: the application lifecycle quadrant

> Referentie uit het Weolcan Cloud Governance Framework (WCGF). Niet Bas zijn eigen IP, hier bewaard als naslag.

the framework's placement model takes the application landscape as the starting point and asks which infrastructure plus service type best fits each phase of the application lifecycle. Applications are distinguished along two axes: Mission Critical vs Non-Mission Critical, and Competitive vs Commodity.

- **Competitive applications** let the company differentiate from competitors, often providing a Unique Selling Point that attracts new customers and better serves existing ones.
- **Commodity applications** support the production process or logistics chain; this is where the money is made.

The two axes form a quadrant mapping the four phases of the application lifecycle:

1. **Invent corner (bottom left).** New applications are developed here. Many attempts fail, so this phase needs infrastructure that switches on quickly and off just as quickly: Public Cloud is very useful here.
2. **Deploy to Scale (top left).** A successful new application is scaled up. It has become Mission Critical, so availability and security requirements rise; this is typically where Managed (cloud) Services are added. The adage is 'Built to Change', responding quickly to new customer wishes, marketing-campaign capacity or seasonal influence, but with a solid SLA.
3. **Manage Scale (top right).** The application's functionality no longer provides competitive advantage; it has become a commodity. Most legacy applications reside here. Infrastructure is 'Built to Last' with as few changes as possible; a Private Cloud is the most frequently used infrastructure here.
4. **Offload (bottom right).** Applications still needed but deserving less time and attention. Procuring this functionality as Software-as-a-Service is usually the best choice.

Classifying applications into these quadrants gives clear insight into what infrastructure ideally fits each application. Part of the WCGF Strategy section; connects to the Application Baseline, Financial Baseline and Cloud Strategy.

*Bron: Salomon-IT 'Cloud Placement Decisions - Cloud Governance'.*

## Verwante notities

- [Application Baseline: purpose and scope](application-baseline-purpose-and-scope.md)
- [Purpose of the cloud financial analysis (business case)](cloud-financial-analysis-purpose.md)
- [Commodity vs competitive applications as the core strategy lens](commodity-vs-competitive-application-lens.md)
- [Landing zone selection dimensions and the decision tree](landing-zone-selection-dimensions.md)
- [The point of cloud strategy is to free IT from commodity toil](position-free-it-ops-from-commodity-burden.md)
- ['Keeping the lights on' starves innovation; offload commodity to fix it](position-keeping-the-lights-on-starves-innovation.md)
- [Service-model preference: SaaS over PaaS over IaaS](service-model-preference-saas-paas-iaas.md)
