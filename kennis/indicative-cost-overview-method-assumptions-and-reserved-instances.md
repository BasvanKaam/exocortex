---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-11
tags: [consulting, kosten, business-case, azure, method]
layer: reference
gedateerd: nee
bron: salomon-opdrachten
---

# Indicative cost overview: split the totals, show the assumptions, never call it a quote

When I attach numbers to an advice report, I do it as an **indicative cost overview**, and I am explicit that it is a global proposal, not a quote ("no rights can be derived from these figures; products and prices change").

## How I structure it
- **Two separate tables, two separate subtotals**: (1) infrastructure / backend components, (2) licenses / software / services. Each line gets a description of the sizing assumption (machine type, vCPU/RAM, disk tier, redundancy, retention) and an estimated monthly cost. Then a monthly + yearly subtotal per table, and a combined total at the end. One-off costs (e.g. perpetual Office licenses) are listed separately and kept *out* of the recurring total so they don't distort it.
- **A "toelichting" (explanation) block under each table** that states region, pricing basis (list prices, vendor calculator), and every modeling assumption.

## The honesty mechanics that make it credible
- **Reserved-instance reasoning, quantified**: I default the estimate to 1- or 3-year reserved instances and state the saving in a number ("~40% versus pay-as-you-go on a yearly basis"). But I also say the **first test phase runs on pay-as-you-go** precisely because you can scale up/down and switch machines off, which minimizes cost while quantities are still unknown.
- **Flag every estimate as an estimate**: where the count of app servers, licenses, or users isn't pinned down, I write "(estimate)" and "costs may turn out higher or lower". I never launder a guess into a hard number.
- **"n.t.b." / to-be-determined is a valid cell value**: services where the cost genuinely can't be known up front (log-analytics-dependent monitoring, Office 365 backup, optional firewall) are listed with the cost left open and the reason given, rather than omitted or invented.
- **Sizing rationale stated**: e.g. why scale-out into several smaller hosts (limit blast radius of one host failing) rather than one big one; why a given machine family.
- **Phasing caveat on the total**: the headline total applies to a *fully delivered, operational* environment; when you start small the first months are far cheaper. I say this so nobody reads the total as month-one spend.

The through-line: numbers are allowed and useful, but every number carries its assumption and its uncertainty next to it. That is what separates an honest indicative overview from a fake-precise quote.

*Bron: geanonimiseerde aanpak uit een Salomon-IT klantopdracht (childcare organization (multi-location childcare provider)).*

## Verwante notities

- [Advice report structure: current-state and advice mirror the same layers](advice-report-structure-current-state-mirrors-advice.md)
- [Anatomy of a Fixed-Price Advisory Proposal](advisory-proposal-anatomy.md)
- [Autoscaling can beat Reserved Instances, and pairs with them](autoscaling-vs-reserved-instances.md)
- [How Azure Reserved Instances and Hybrid Benefit work](azure-ri-ahb-mechanics.md)
- [How Bas Structures a Cloud Proposal: Recap, Then Scenarios, Then Split Costs](bas-proposal-structure-recap-then-scenarios.md)
- [Cloud business case: TCO to ROI, with the soft variables named](cloud-tco-roi-business-case.md)
- [The 'conclusion and next steps' pattern with split effort estimates](conclusion-and-next-steps-effort-estimates.md)
- [A simple DIY method to compare Cloud datacenter latency](diy-cloud-latency-ping-test-method.md)
- [IST/SOLL report skeleton](ist-soll-report-skeleton.md)
- [Start small, test, then scale — because it de-risks the client's investment](position-start-small-test-then-scale-derisks-investment.md)
- [How I structure a transformation offer and its costing](transformation-offer-costing-model.md)
- [Two-scenario advice and recommendation principles](two-scenario-advice-and-recommendation-principles.md)
- [The Two-Scenario Offer: Centralized Backend vs Managed-Laptop-Only](two-scenario-offer-pattern.md)
