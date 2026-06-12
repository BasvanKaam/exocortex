---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-11
tags: [proposal, offer, deliverable-template, consulting-method, salomon, business-case]
layer: reference
gedateerd: nee
bron: salomon-opdrachten
---

# How Bas Structures a Cloud Proposal: Recap, Then Scenarios, Then Split Costs

A reusable skeleton distilled from Bas's written cloud/managed-services proposals. The order is deliberate: ground the reader in their own situation first, only then offer options, only then price.

**1. Warm opener.** Thank the client for their time and the "gezellig" conversation, and apologize in advance for any typos. The relationship tone is set before any tech. Bas notes that the "gevoel" being right matters and says so explicitly.

**2. Meeting recap ("Samenvatting gesprek <date>").** Play back the current situation in the client's own words: what they run today, what they are happy with, what drives them, and the named primary goal (e.g. "kostenbesparing met behoud van functionaliteit"). This proves you listened and anchors everything that follows.

**3. Current-state overview + application list.** A bullet inventory of the existing environment (workloads, identity, mail, data, endpoints) and a small table: application name -> where and how it runs.

**4. Item -> possible-approach mapping table.** Each current component on the left, the proposed cloud-or-not approach on the right (e.g. Citrix -> WVD + IaaS; on-prem Exchange -> Exchange Online; file/print -> SharePoint/OneDrive). This is the heart of the recommendation and reads at a glance.

**5. Two scenarios with onderbouwing.** See the companion note on the two-scenario pattern. Each design choice gets a short justification paragraph.

**6. Costs, deliberately split into four buckets** so the client can reason about each independently:
   - monthly infrastructure (built from the cloud provider's own calculator, region stated, reserved-instance discount and its prepay catch flagged)
   - monthly licenses (per user)
   - one-off licenses/tooling (e.g. a migration tool)
   - one-off inventory/migration/build effort as an hours x rate table per workload
   He states base assumptions plainly (list prices; an external party not yet familiar with the environment; full cooperation from the incumbent assumed; design/documentation excluded unless scoped).

**7. Points of attention ("Overig").** Honest caveats: latency risk in cloud/WVD and the standing advice to test thoroughly before go-live; tenant-migration unknowns; where specialist third-party advice is needed; tooling and backup-product preferences with the reason (good prior experience), always leaving room for an alternative.

**8. How to proceed.** Name the next step and the contact, and reaffirm transparency: ask anything anytime, and you are welcome to shadow us to pick up knowledge during the transition.

For management, Salomon can also deliver a one-page-per-pillar summary, and always a presented end report with lessons learned at project close.

*Bron: geanonimiseerde aanpak uit een Salomon-IT klantopdracht (private-equity / investment firm (and, in the same engagement file, a food-research institute) — both small-to-mid organizations evaluating a managed-services and cloud migration).*

## Verwante notities

- [Advice report structure: current-state and advice mirror the same layers](advice-report-structure-current-state-mirrors-advice.md)
- [Anatomy of a Fixed-Price Advisory Proposal](advisory-proposal-anatomy.md)
- [Cloud business case: TCO to ROI, with the soft variables named](cloud-tco-roi-business-case.md)
- [Indicative cost overview: split the totals, show the assumptions, never call it a quote](indicative-cost-overview-method-assumptions-and-reserved-instances.md)
- [How I structure a transformation offer and its costing](transformation-offer-costing-model.md)
- [The Two-Scenario Offer: Centralized Backend vs Managed-Laptop-Only](two-scenario-offer-pattern.md)
- [Proposal structure: conversation recap plus first impression under reservation](voorstel-structuur-eerste-indruk.md)
