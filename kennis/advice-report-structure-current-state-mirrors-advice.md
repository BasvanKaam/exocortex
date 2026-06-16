---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-11
tags: [consulting, advice, rapportstructuur, assessment, method]
layer: reference
gedateerd: nee
bron: salomon-opdrachten
---

# Advice report structure: current-state and advice mirror the same layers

My workplace/infrastructure advice reports follow one fixed skeleton, and the trick that makes them readable is that the **advice section mirrors the current-state analysis section layer for layer**. The reader meets each topic twice: once as "this is how it is now", then again as "this is what I propose".

## The skeleton
1. **Introduction** — goal of the research (one sentence: deliver advice on X that fits the functional need, IT strategy and policy of the client), approach (how the information was gathered), and report distribution (need-to-know internally, client-only externally, no further distribution without client approval).
2. **Management summary** — who the client is, complexity verdict in plain words (e.g. "average complexity", "varied but not extremely complex"), what triggered the request (often a health check that surfaced aged hard/software), what the client wants, and the guiding principles (e.g. flexibility, standardization, separating need from nice-to-have).
3. **Assessment interviews** — see the separate interview-method note.
4. **Current-state analysis** — organized by a fixed set of layers (see below).
5. **Advice** — opens with a short list of the *needs* distilled from the interviews, then walks the **same layers in the same order** as the analysis.
6. **Indicative cost overview** — see the separate cost-overview note.
7. **Comparison with the current environment** — a current-vs-new table (see the separate note).
8. **Global approach / phasing** — the staged rollout, closed with the 0.9 presentation step.

## The fixed layers (used in both analysis and advice)
- Locations
- Workplace, physical
- Workplace, virtual
- Application landscape, data and licenses
- Backend / infrastructure
- Network / infrastructure
- Account management, support and external access
- Security
- Backup and disaster recovery

## Habits that travel
- **Need-to-know distribution** stated up front, marked confidential.
- **Honest gaps**: where a current-state table may be stale or quantities are unknown, I say so explicitly ("this overview may be outdated, further investigation needed") rather than pretending completeness.
- **Scope discipline with a courtesy flag**: when something useful surfaces that is out of scope, I note it as out of scope but still bring it to attention (e.g. an end-user complaint about a phone provider).
- **Defer detail honestly**: the advice repeatedly says "this is worked out further in a technical/functional design" rather than over-promising precision the intake can't support.

*Bron: geanonimiseerde aanpak uit een Salomon-IT klantopdracht (childcare organization (multi-location childcare provider)).*

## Verwante notities

- [Assessment interview method: kick-off plus a fixed end-user questionnaire](assessment-interview-method-kickoff-plus-fixed-questionnaire.md)
- [How Bas Structures a Cloud Proposal: Recap, Then Scenarios, Then Split Costs](bas-proposal-structure-recap-then-scenarios.md)
- [The 'conclusion and next steps' pattern with split effort estimates](conclusion-and-next-steps-effort-estimates.md)
- [Engagement structure: workplace and infrastructure assessment](engagement-structure-workplace-infra-assessment.md)
- [Indicative cost overview: split the totals, show the assumptions, never call it a quote](indicative-cost-overview-method-assumptions-and-reserved-instances.md)
- [My intake method: per-service IST/SOLL gap analysis with MoSCoW and coverage scoring](intake-ist-soll-gap-analysis-method.md)
- [IST/SOLL report skeleton](ist-soll-report-skeleton.md)
- [How Bas structures a research/advisory report (onderzoeksrapport)](research-advisory-report-structure.md)
- [Two-scenario advice and recommendation principles](two-scenario-advice-and-recommendation-principles.md)
- [Proposal structure: conversation recap plus first impression under reservation](voorstel-structuur-eerste-indruk.md)
