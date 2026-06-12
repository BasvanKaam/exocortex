---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-11
tags: [cloud-governance, application-baseline, assessment-method, wcgf, discovery]
layer: reference
gedateerd: nee
attributie: weolcan-wcgf
bron: salomon-cloud-governance
---

# Two-phase scan method for the Application Baseline

> Referentie uit het Weolcan Cloud Governance Framework (WCGF). Niet Bas zijn eigen IP, hier bewaard als naslag.

The method runs the application baseline as a deliberate two-pass approach, trading speed against resolution.

**Scan 1: high level | high speed | low resolution.** The first pass works at high speed and high abstraction. Avoid details; the goal is a high-level view and understanding. Identify bundles of applications that form logical groups based on shared architecture patterns or because they belong to the same set. Earmark the bundles that show cloud potential for review in the next phase.

Tooling for Scan 1:
- Automated application discovery tools (AWS Application Discovery Service, Microsoft MAP, Cloudamize) to non-intrusively report infrastructure footprint, installed applications and inter-application relationships, producing standardized output that speeds the assessment.
- Electronic questionnaires (SurveyMonkey-style) to question many application owners at once, sometimes letting owners update application data directly.
- Other data sources: sizing pulled from management control interfaces (e.g. storage allocation exports, VM inventory from VMware vCenter or RVtools).

**Scan 2: low level | low speed | high resolution.** A detailed assessment of only the bundles that showed great cloud potential. Run detailed analysis workshops with the teams responsible for the applications, prepared by modelling gathered information into an enterprise architecture methodology like ArchiMate. The goal: determine how applications are constructed, which platforms and technologies they rely on, what the strategic drivers for migration are, which components have potential for cloud services (managed or serverless), and what the roadblocks are (technology or configuration choices incompatible with cloud).

**Reporting.** Pay attention to dominant platforms (database, middleware, programming platforms) and identify outliers on less modern technology. Establish the dominant technology choices and their cloud readiness, and which applications are used by which business department.

*Bron: Salomon-IT 'Application Baseline - Cloud Governance'.*

## Verwante notities

- [Application Assessment Canvas](application-assessment-canvas.md)
- [Application Baseline: purpose and scope](application-baseline-purpose-and-scope.md)
- [Enterprise Architecture (EA) and TOGAF](enterprise-architecture-togaf.md)
- [Growth Assessment: baseline, future state, gap](growth-assessment-baseline-gap.md)
- [Joint Inventory: Two Pairs of Eyes Beat One](joint-inventory-two-pairs-of-eyes.md)
- [Good-enough beats perfect: avoid analysis paralysis](position-good-enough-assessment-over-analysis-paralysis.md)
- [SCAF: Application, Data and System Inventory via Waves](scaf-application-data-system-inventory.md)
