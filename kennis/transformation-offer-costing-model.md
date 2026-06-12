---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-11
tags: [offerte, kosten, tarieven, risico-bandbreedte, sla, scoping]
layer: reference
gedateerd: nee
bron: salomon-opdrachten
---

# How I structure a transformation offer and its costing

How I build and present the priced offer that comes out of the analysis phase.

## Split one-off from recurring, always
I separate the two cost types and never blur them:
- **One-off transformation cost** — the hours for all the one-time work to build and move the services, billed to the client.
- **Recurring exploitation cost** — the yearly run cost of the delivered services.
For a later plateau that is not yet fully analysed I still give an **indicative** figure, clearly labelled as indicative, plus a combined total. Better a flagged estimate than a silent gap.

## Tariff logic: generic / specific / custom
Three delivery types, each priced differently, and I map every service to one:
- **Generic** — standardised, deliverable to all clients, **fixed tariff**, billed on volume consumed.
- **Specific** — per-client, billed **afterwards on actual cost** (nacalculatie).
- **Custom** — finite work (projects, consultancy), billed via a **separate offer** with a scope and an estimate.

## Anchor the cost to drivers (kengetallen)
Every per-service cost line is anchored to explicit cost drivers / key figures (counts, volumes, server sizes) listed in the document, so the price is reconstructable and re-negotiable when reality differs. Server sizing itself I drive off a simple points formula (e.g. points = 4 x #CPU + memory in GB -> Small/Medium/Large/Special) rather than ad-hoc.

## Build a risk bandwidth into the numbers
The cost is an estimate based on analysis-phase information, so I state a **risk bandwidth** (here 15%) for steering, reporting and decision-making, and I report realisation against the estimate **and** the bandwidth in the steering group. This sets the expectation that the estimate will move, before it moves.

## State assumptions, exclusions and license split explicitly
- Cost is based on a stated **lead time** (e.g. 20 weeks); a longer lead time costs more, said out loud.
- I list which **licenses the client must supply** themselves vs which are inside the service price.
- Variable usage costs (print per page, telephony per user) are named separately, not hidden in the service price.
- Tariffs are dated ("based on this year's catalogue, revised yearly").

*Bron: geanonimiseerde aanpak uit een Salomon-IT klantopdracht (a government ICT shared-service center onboarding a public-sector research/policy institute).*

## Verwante notities

- [Anatomy of a Fixed-Price Advisory Proposal](advisory-proposal-anatomy.md)
- [How Bas Structures a Cloud Proposal: Recap, Then Scenarios, Then Split Costs](bas-proposal-structure-recap-then-scenarios.md)
- [Indicative cost overview: split the totals, show the assumptions, never call it a quote](indicative-cost-overview-method-assumptions-and-reserved-instances.md)
- [SCAF TCO / Business-case template](scaf-tco-business-case-template.md)
- [Transition/transformation engagement structure: intake, analyse, execute in plateaus](transition-transformation-engagement-structure.md)
- [The Two-Scenario Offer: Centralized Backend vs Managed-Laptop-Only](two-scenario-offer-pattern.md)
