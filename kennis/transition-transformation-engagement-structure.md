---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-11
tags: [consulting-aanpak, migratie, transformatie, fasering, governance]
layer: reference
gedateerd: nee
bron: salomon-opdrachten
---

# Transition/transformation engagement structure: intake, analyse, execute in plateaus

How I structure a large IT sourcing/migration engagement (moving an organization's ICT services onto a provider platform). Three sequential phases, each ending in a signed document that gates the next.

## Phase 1 — Intake
A short scoping phase. Output is an intake report that fixes the scope of services the receiving organization intends to take, plus a high-level roadmap. This is where I decide the coarse cut: what is in, what is out, what is already running. Nothing detailed is promised yet.

## Phase 2 — Analysis
The heavy phase (in this engagement, roughly 8 months). Inventory the current ICT services, map them against the provider's standard service catalogue, decide per service whether the standard covers it or custom work is needed. Output is two deliverables that go to the steering group together:
- an **offer** (the priced execution proposal), and
- a **transition/transformation plan** (the how, per service, with planning and budget).

## Phase 3 — Execution
Only starts after the offer is signed. The signed offer is the gate: it is conditional for every following step.

## Plateaus, not one big move
I split the move into **plateaus** (typically three). Each plateau states exactly which services move in it. Plateau 1 is often already-running quick wins that I treat as part of the current (IST) situation for planning purposes. The analysis-heavy or higher-risk services (e.g. compute/research workloads) get their own later plateau and are re-analysed before they move.

## The 5 execution steps (per plateau)
1. **Decision & contracting** — steering group approves the plan; signed offer starts the work.
2. **Initiation** — detailed/technical design, per-service test & acceptance plan, migration and fall-back plan, order hardware/software/licenses. Re-verify the analysis-phase data against current reality and assess the impact of any drift.
3. **Build & test** — build environments, run user tests then acceptance tests, train admins and the support desk, let users meet the new workplace early.
4. **Go-live** — migrate accounts and data, cut over, communicate, aftercare, hand over to operations.
5. **Closure** — delivery protocol and discharge report.

## Why this shape
The phase gates keep the client deciding at the right moments (scope, then price, then go), and the plateaus spread migration risk over time so a mistake in one step is contained and the fall-back per step stays simple.

*Bron: geanonimiseerde aanpak uit een Salomon-IT klantopdracht (a government ICT shared-service center onboarding a public-sector research/policy institute).*

## Verwante notities

- [Cloud inventory method: joint assessment, waves, and the R's](cloud-inventarisatie-methode-waves-en-rs.md)
- [Engagement structure: from first conversation to handover](engagement-structure-presales-to-handover.md)
- [My intake method: per-service IST/SOLL gap analysis with MoSCoW and coverage scoring](intake-ist-soll-gap-analysis-method.md)
- [Migration strategy framework: transition vs transformation, big-bang vs phased, build-clean-alongside](migration-strategy-decision-framework.md)
- [SCAF timeline: phases, deliverables and gates](scaf-timeline-phases-deliverables-gates.md)
- [How I structure a transformation offer and its costing](transformation-offer-costing-model.md)
- [Principles I apply on transformation engagements](transformation-principles-positions.md)
