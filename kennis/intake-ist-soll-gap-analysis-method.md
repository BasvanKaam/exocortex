---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-11
tags: [intake, assessment, gap-analyse, moscow, requirements, interviews]
layer: reference
gedateerd: nee
bron: salomon-opdrachten
---

# My intake method: per-service IST/SOLL gap analysis with MoSCoW and coverage scoring

How I inventory and assess an existing IT estate before proposing a target state. The core trick: I never assess "the environment" as a blob. I cut it into discrete **services** and run the same template over each one.

## Three inventory instruments
I gather the current state with three complementary instruments, not one:
1. **Questionnaires** — structured, so I get comparable data.
2. **Interviews** — with functional and technical admins, key users, owners.
3. **Site visits** — to see what the paper does not say.

Government estates are usually organically grown and poorly documented, with no clear owner per application. So I derive the application list from the organization's stated **information-provision (IV) functions** rather than trusting an existing inventory, and I flag missing owners as a finding.

## The per-service template (IST -> SOLL)
For every service I write the same sections:
- **IST** — current situation, strictly from client-supplied info (and I say so).
- **Service description** — the provider's standard service and which standard building blocks it is made of.
- **Architecture & security requirements** specific to this service.
- **SOLL** — how the target service is delivered, and how each gap between IST and SOLL is bridged.
- **Transformation** — how this service actually moves.
- **Contractual items**, **opportunities**, **risks**, **dependencies**.

## Requirements scoring I apply
- Client requirements are classified **MoSCoW** (Must/Should/Could/Won't).
- Per requirement I score coverage with a simple three-way signal: covered / partially covered (gap to be investigated) / not delivered. A visual marker (a smiley in the report) makes the gaps jump off the page for a non-technical steering group.

## Honesty markers I always include
- State explicitly when a count or list is client-supplied and **not** independently verified (e.g. "the client hardware list was not checked in detail").
- Carry numbers that illustrate scale (volumes, counts, TB) but treat them as estimates to be re-inventoried in execution.

This template is what makes the later offer defensible: every euro in the price traces back to a scored requirement and a named gap.

*Bron: geanonimiseerde aanpak uit een Salomon-IT klantopdracht (a government ICT shared-service center onboarding a public-sector research/policy institute).*

## Verwante notities

- [Advice report structure: current-state and advice mirror the same layers](advice-report-structure-current-state-mirrors-advice.md)
- [Four-Step Assessment-to-Roadmap Engagement Structure](assessment-to-roadmap-engagement-structure.md)
- [Cloud-migration suitability checklist for client/server applications](cloud-migration-suitability-checklist-client-server-apps.md)
- [A cloud GAP analysis must end in a sourcing decision, not just a skills delta](gap-analysis-is-a-sourcing-decision.md)
- [IST/SOLL report skeleton](ist-soll-report-skeleton.md)
- [SCAF GAP-analysis worksheet: SOLL vs IST across five sourcing dispositions](scaf-gap-analysis-worksheet.md)
- [Transition/transformation engagement structure: intake, analyse, execute in plateaus](transition-transformation-engagement-structure.md)
