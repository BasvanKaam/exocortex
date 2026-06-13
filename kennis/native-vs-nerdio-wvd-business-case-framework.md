---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [nerdio, wvd, business-case, azure-cost, autoscale]
layer: reference
gedateerd: nee
bron: nerdio-blog
---

# Framing a native-vs-Nerdio WVD business case

His reusable structure for building a WVD/Nerdio business case (the method, not the numbers):

1. Profile the scenario concretely: user count, concurrency, on-prem vs cloud today, multi-session vs personal, GPU/SKU, storage tier (Premium SSD OS disk, Azure Files Premium), and weekly intensive-usage hours. A specific profile makes the cost comparison credible.
2. List the situation and requirements as the customer would: reuse existing WVD without rebuild/reassign, migrate v1 (non-ARM) to v2 (ARM), enterprise image/application management within a few hours a week, low PowerShell skill, minimal Azure expertise, tight budget, secure connections, HA, data ownership, and time pressure.
3. State current challenges: aging hardware, over/under-provisioning, unused capacity, slow hardware procurement (weeks to months), manual machine lifecycle, work-from-home secure-access gaps, login failures from resource shortage or boot delays, limited IT staff and budget.
4. Contrast native WVD vs Nerdio-powered point by point: setup time (week+ vs hours), workforce enablement (Nerdio lets the bulk of IT staff manage/optimize WVD daily without deep PowerShell), onboarding/migration of existing tenants, event-driven autoscale with host pre-staging and auto-heal, predictable cost vs PAYG, user session management/shadowing, image management (import VMs/Marketplace/SIG/custom, backup, cloning, versioning, scheduled auto-update, MSIX App Attach), native-service integrations (FSLogix, Azure Files), HA via Availability Sets/Zones and multi-region/split-tenant, end-user self-service start/stop/restart, auditing and Azure monitoring, and right-sizing recommendations.
5. Land on time-to-value (weeks to hours) and a cost-saving percentage per user per month.

The core argument: WVD's value is real but its setup time and unpredictable ongoing Azure cost make it a hard sell to management; Nerdio removes both barriers.

*Bron: Nerdio-content 'NMW Business Case - draft' (Blogs).*

## Verwante notities

- [The real win of WVD automation is reclaimed admin time, not just compute](automation-saves-time-equals-money-position.md)
- [The Real Blocker to AVD Adoption Is the Cost Conversation](avd-adoption-is-blocked-by-the-cost-conversation.md)
- [AVD cost-component breakdown](avd-cost-component-breakdown.md)
- [AVD Cost Modelling: Modeler + User Cost Attribution](avd-cost-modelling-modeler-and-cost-attribution.md)
- [Idea: NMW Blog/Content Backlog](idee-nmw-blog-backlog.md)
- [Lead with operational and business value; cost savings is the cherry on top](lead-with-operational-value-not-just-cost.md)
- [Building an MSP cloud practice rests on three pillars](msp-cloud-practice-three-pillars.md)
- [The NMW thesis: automation and hiding complexity](nmw-thesis-automation-hiding-complexity.md)
- [WVD's value is blocked by setup time and unpredictable cost](position-wvd-value-blocked-by-cost-and-complexity.md)
- [WVD with Nerdio on top is the new 'RDS with Citrix on top'](wvd-with-nerdio-on-top-citrix-framing.md)
