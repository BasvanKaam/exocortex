---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-11
tags: [business-case, tco, roi, cloud-economics, opex-capex, method]
layer: reference
gedateerd: nee
bron: salomon-opdrachten
---

# Cloud business case: TCO to ROI, with the soft variables named

How I structure a cloud migration business case so it's defensible and honest about what's estimated.

## The calculation
1. **Current TCO.** Application + infrastructure: development, maintenance, licences, middleware, OS, virtualisation, plus the full on-prem cost stack (hardware, power, cooling, security, premises, cabling, refresh cycles, support contracts).
2. **Transition (one-off) costs.** Development, data migration or rebuild, and the temporary overlap between old and new. One-off.
3. **Cloud TCO.** Hours in use (estimated), maintenance, user count, data volume, licences / subscription.
4. **Business case (ROI).** `Current TCO - Cloud TCO = difference`. Then `(difference - one-off costs) / one-off costs = ROI`. That difference is what makes the business case.

## Be explicit about what's estimated
I mark clearly which inputs are estimates (cloud usage hours, part of the transition cost) and which are calculator-backed. I don't present a guess as a fact. Vendor/community calculators exist for parts of this; I use them rather than inventing numbers.

## Don't let the case rest on price alone
The variables that are hard to quantify still belong in the case, named as such: Opex vs Capex, elastic scale up/down, time-and-place independence, pay-per-use. I deliberately steer the conversation off a pure cost focus and onto the broader value of cloud, because a price-only story loses to the incumbent on the wrong day.

## Illustrative figures I've used
- Autoscaling on workplace compute: averaging ~70%+ savings on the underlying resources.
- Reserved instances: lock 1-3 years, with a penalty (~12%) on the remaining term if you exit early.
- Right-size VMs (scale out or up), pick the workload-appropriate VM type (sometimes trial and error), monitor cost, set alarms, tag resources.

## Related
- See `engagement-structure-presales-to-handover.md` (business case lives in the proposal phase).
- See `cloud-fit-compare-cloud-to-cloud.md` for the comparison baseline.

*Bron: geanonimiseerde aanpak uit een Salomon-IT klantopdracht (an IT managed services provider (cloud workplace reseller)).*

## Verwante notities

- [Bas's method: launch a new technology practice on four parallel tracks](bas-launching-a-new-tech-practice-four-tracks.md)
- [Bas on cost management: cost vs. value and ROI/TCO](bas-on-cost-management-roi-tco.md)
- [How Bas Structures a Cloud Proposal: Recap, Then Scenarios, Then Split Costs](bas-proposal-structure-recap-then-scenarios.md)
- [The defaults-exposing cloud financial business case](cloud-financial-business-case-defaults.md)
- [Compare cloud to cloud, not cloud to on-prem](cloud-fit-compare-cloud-to-cloud.md)
- [Building a Compact Cloud Business Case](compact-cloud-business-case-method.md)
- [If cost saving is your primary cloud driver, reconsider your strategy](cost-saving-is-the-wrong-primary-cloud-driver.md)
- [Discovery and qualification: the questions I ask](discovery-qualification-questions.md)
- [Engagement structure: from first conversation to handover](engagement-structure-presales-to-handover.md)
- [Hard costs vs soft costs (both matter)](hard-costs-vs-soft-costs.md)
- [Indicative cost overview: split the totals, show the assumptions, never call it a quote](indicative-cost-overview-method-assumptions-and-reserved-instances.md)
