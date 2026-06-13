---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-11
tags: [cloud-exit, scaf, cloud-strategy, vendor-lock-in, migration]
layer: reference
gedateerd: nee
bron: salomon-it-blog
---

# Cloud Exit Strategy: What to Plan For

A cloud exit strategy is a plan for moving (at least part of) your applications, data and systems away from a Cloud Service Provider, prepared in advance even while you are happily committing to that provider. The reasoning: you should not assume you will need it, but you must account for it. Triggers can include dissatisfaction, a provider breaking agreements, a provider stopping services without explanation or going bankrupt, cost reconsideration, disappointing quality, or a shift in IT/business strategy. Applies to both existing and future cloud environments.

Work in an organized way and break the whole into smaller steps. Key points of attention (non-exhaustive, in practice the list is at least three times as long, and each point carries a counter-weighing, possible action or alternative):

- **Inventory.** Know exactly which services are consumed and how, in as much detail as possible. Map dependencies between components/systems/applications: can one exist without the other? Beware the common gap where an organization 'assumes' it runs X applications/systems but the real count turns out to be 40% higher.
- **PaaS and SaaS lock-in.** These services are often very specific and deeply rooted in the underlying infrastructure, so you cannot 'just' move them between platforms. The more generic the approach, the more flexible the workload. The trade-off: PaaS/SaaS often deliver the largest and fastest gains. Weigh it up.
- **Licenses.** Reuse of existing on-premises licenses is often permitted, but rules and fine print change continuously.
- **Data export format.** In which format can data be exported or downloaded? Not all formats are supported by all platforms. Can agreements be made about this?
- **Data volume vs. time.** When you leave or a provider fails, you often have limited time (e.g. 30 to 60 days) to extract everything. For petabytes or hundreds of TB that may not be enough. Rule of thumb: amount of data + available time + throughput = export feasibility. Data grows unnoticed, so monitor it and know the conditions.
- **Provider rules and SLAs.** Rules around cloud service use differ per provider and can change mid-contract; SLAs are usually fairly transparent. Cancelling certain services may suddenly remove access to 'extras' you relied on.
- **Cost and duration of A-to-B.** Estimate roughly what it costs and how long it takes to move, so you are not surprised if it ever comes to it.
- **Upstream SLA obligations.** Coming from a managed service provider situation, you may have SLA commitments toward your own user organizations, plus other contracts or agreements.
- **Choosing the replacement.** Do not pick an alternative 'just like that'. Impact can be large; assess your organization's current knowledge level. This is the moment to think carefully about the next step so you do not face the same challenge again in two years.

Method note: the exit-strategy model can be applied to existing and future cloud environments and is part of the SCAF, or used standalone.

Source: Bas van Kaam, Salomon IT blog, 2019-08-28.

*Bron: blogpost 'Wat een Cloud exit strategie inhoudt? Het SCAF?' (2019-08-28), salomon-it.nl.*

## Verwante notities

- [Exit flexibility depends on the cloud service model (IaaS/SaaS/PaaS)](cloud-exit-flexibility-by-service-model.md)
- [Bas's checklist of points of attention for a cloud exit](cloud-exit-points-of-attention.md)
- [Cloud Exit Strategy (start with the exit)](cloud-exit-strategy-cheat-sheet-idea.md)
- [Why have a cloud exit strategy - the exit comes before onboarding](cloud-exit-strategy-rationale.md)
- [The six-step process for building a cloud exit strategy](cloud-exit-strategy-steps.md)
- [Plan the Exit Before You Commit](plan-the-exit-before-you-commit.md)
- [A Cloud Strategy without a reversibility plan is incomplete](position-cloud-strategy-needs-exit-strategy.md)
- [SCAF Cloud Exit Strategy Template (On Bas's Backlog)](scaf-cloud-exit-strategy-on-backlog.md)
