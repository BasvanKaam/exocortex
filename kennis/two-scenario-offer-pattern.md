---
type: positie
merk: bvk
domein: cloud
status: actief
datum: 2026-06-11
tags: [positie, proposal, decision-framework, consulting-method, salomon, managed-laptop]
bron: salomon-opdrachten
---

# The Two-Scenario Offer: Centralized Backend vs Managed-Laptop-Only

A recurring decision device in Bas's small-org cloud proposals: rather than pushing one design, he lays out **two scenarios** and lets the client choose. "Wij geven het inzicht, jij maakt de juiste keuze" applied to the offer itself.

The two poles he consistently frames:
- **Scenario 1 - thin centralized backend.** A small WVD/multi-session estate plus minimal IaaS (e.g. a couple of lightweight VMs for domain controllers, one VM for an app + its database). User data to OneDrive, department data to SharePoint, mail to Exchange Online. This keeps a familiar central environment.
- **Scenario 2 - managed-laptop-only, no backend.** Intune + the modern-management stack (modern license bundle, autopilot) deliver a fully managed laptop as the primary device, with all required software baked into the image. No domain controllers, no session hosts, no app-server VMs.

The judgement that drives the framing: when the application landscape is thin and the environment small, a published full desktop (Citrix-style) is overkill, and once collaboration lives in SharePoint/Teams the central desktop becomes largely redundant. So both scenarios are realistic and the choice is genuinely open.

The sharp economic insight he attaches: in scenario 2 a pricier SaaS edition of a core app (which might look unaffordable in isolation) is offset because **the entire central backend falls away, freeing budget to absorb it.** Don't price components in isolation; price the whole stack per scenario so trade-offs become visible.

Keep the rest constant. Decisions on user/department data, mail, backup, licenses and support are held identical across scenarios, so the client compares only the variable that matters.

*Bron: geanonimiseerde aanpak uit een Salomon-IT klantopdracht (private-equity / investment firm (and, in the same engagement file, a food-research institute) — both small-to-mid organizations evaluating a managed-services and cloud migration).*

## Verwante notities

- [How Bas Structures a Cloud Proposal: Recap, Then Scenarios, Then Split Costs](bas-proposal-structure-recap-then-scenarios.md)
- [Positions I apply in a cloud transition](cloud-transitie-posities.md)
- [Full Cloud Migration Is Rarely a Good Idea](full-cloud-is-rarely-a-good-idea.md)
- [We Give the Insight, You Make the Choice](give-insight-client-decides.md)
- [Indicative cost overview: split the totals, show the assumptions, never call it a quote](indicative-cost-overview-method-assumptions-and-reserved-instances.md)
- [How I structure a transformation offer and its costing](transformation-offer-costing-model.md)
- [Two-scenario advice and recommendation principles](two-scenario-advice-and-recommendation-principles.md)
