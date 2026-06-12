---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [consulting, report-structure, ist-soll, current-state, target-state, method, template]
layer: reference
gedateerd: nee
bron: salomon-opdrachten
---

# IST/SOLL report skeleton

The chapter skeleton I reuse for a workplace/infrastructure advisory report. Sections that do not apply get dropped, not faked; rename or reorder sensibly per engagement.

## IST (current state) chapters
Walk the environment top to bottom so nothing is missed:
- **General** and **locations** (always give a site overview, even for a single site).
- **The workplace, physical** and **the workplace, virtual** (name the underlying platform: Citrix, Microsoft, VMware).
- **Application landscape, data, collaboration and licensing.** Put the application landscape in a table, then annotate it. Flag when the inventory is not yet complete, and call out concurrency: a large share of apps are often used by a handful of users, so concurrent use is lower than the headcount suggests, which has cost consequences.
- **Backend infrastructure** (file/print servers, DNS, DHCP, AD, database servers, virtualization hosts), with the domain, virtualization/hypervisor and workload distribution.
- **Network infrastructure** (switches, line types), with a line-connection diagram for secondary sites.
- **User and account management** (who does what, where data and profiles live), **processes**, **external access** (gateway, MFA), **security measures**, and **printing**.
- Close IST with a **current-challenges** summary. This restates, crisply, the problems the advice must solve.

## SOLL (target state) chapters
- Open with a **general** description and the criteria the scenarios must meet.
- Then re-walk the same IST chapter list, but this time with the alternative approach plus a justifying rationale where useful. Sub-topics that do not change are explicitly marked unchanged rather than repeated.
- Quantify with an **indicative cost overview** near the end (see the proposal/cost-conventions note), and keep support and management costs in a separate table, never folded into the total price.

## Why this works
Reusing one skeleton across IST and SOLL means every current-state topic gets an explicit target-state answer, and the reader can map old to new one-to-one.

## Related
- Engagement structure: workplace and infrastructure assessment
- Interview and assessment intake method
- Two-scenario advice and recommendation principles
- Cloud-migration suitability checklist for client/server applications

*Bron: geanonimiseerde aanpak uit een Salomon-IT klantopdracht (property and real-estate services organization (multi-entity, multi-site)).*

## Verwante notities

- [Advice report structure: current-state and advice mirror the same layers](advice-report-structure-current-state-mirrors-advice.md)
- [Four-Step Assessment-to-Roadmap Engagement Structure](assessment-to-roadmap-engagement-structure.md)
- [Cloud-migration suitability checklist for client/server applications](cloud-migration-suitability-checklist-client-server-apps.md)
- [The 'conclusion and next steps' pattern with split effort estimates](conclusion-and-next-steps-effort-estimates.md)
- [Detailontwerp (Detailed Design) Document Skeleton](detailontwerp-document-skeleton.md)
- [Engagement structure: workplace and infrastructure assessment](engagement-structure-workplace-infra-assessment.md)
- [Indicative cost overview: split the totals, show the assumptions, never call it a quote](indicative-cost-overview-method-assumptions-and-reserved-instances.md)
- [My intake method: per-service IST/SOLL gap analysis with MoSCoW and coverage scoring](intake-ist-soll-gap-analysis-method.md)
- [Interview and assessment intake method](interview-assessment-method.md)
- [How Bas structures a research/advisory report (onderzoeksrapport)](research-advisory-report-structure.md)
- [Two-scenario advice and recommendation principles](two-scenario-advice-and-recommendation-principles.md)
