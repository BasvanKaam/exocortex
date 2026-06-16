---
type: kennis
merk: bvk
domein: financieel
status: actief
datum: 2026-06-11
tags: [masterclass, business-case, tco, roi, opex-capex, cloud-economics]
layer: reference
gedateerd: nee
bron: salomon-masterclass
---

# Worked TCO/ROI exercise: on-prem vs co-lo vs managed vs IaaS

A teaching exercise the Masterclass uses to make the cloud business case concrete, building beyond the book's conceptual treatment. It costs out an identical small e-commerce stack (2x firewall, 2x load balancer, 2x web/app/database servers, Linux plus open-source, redundant, no staff costs) across four hosting models and compares monthly/yearly cost:
- Own datacenter (on-prem): ~EUR 611/month, EUR 7,332/year (Capex EUR 22,000 amortized, power/cooling/rack assumed already available).
- Co-location: ~EUR 1,111/month, EUR 13,332/year (same Capex plus ~EUR 500/month colo opex, year contract).
- Managed services: ~EUR 2,114/month, EUR 25,368/year (Capex becomes opex, everything rented and included).
- Cloud IaaS: ~EUR 520-813/month, EUR 6,240-9,756/year (all opex, 3-year reserved instances, bandwidth and S3 storage extra).

The deck deliberately surfaces the variables that move these numbers: reserved vs convertible vs on-demand instances, 24x7 availability, no snapshots/backups by default, standard HDD, Linux vs pricier Windows licensing, region pricing (Europe dearer than US), provider differences (AWS/Azure/GCP), machine type, and the option to redesign via PaaS/DaaS/SaaS or the 6 R's. It then layers a DaaS business case with two scenarios (WVD/IaaS backend at EUR 1,369.56/month vs SaaS-only at EUR 765.50/month) to show the spread.

*Bron: Salomon-IT 'MC - Aantekeningen tbv Salomon Cloud Masterclass'.*

## Verwante notities

- [Reading the Hosting Spectrum - Capex Falls, Opex Rises](capex-opex-shift-across-hosting-spectrum.md)
- [Cloud business-case template (eleven dimensions)](cloud-business-case-template-eleven-dimensions.md)
- [Cloud cost-optimization levers](cloud-cost-optimization-levers.md)
- [If cost saving is your primary cloud driver, reconsider your strategy](cost-saving-is-the-wrong-primary-cloud-driver.md)
- [Start a DaaS Business Case 'High-Over' First](daas-business-case-high-over-first.md)
- [From cost model to business case](from-cost-model-to-business-case.md)
- [Is the Cloud Cheaper? It Depends](is-cloud-cheaper-it-depends.md)
- [Comparing a Physical Server to Cloud Isn't Fair](physical-vs-cloud-server-not-fair-comparison.md)
