---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-11
tags: [consulting-tool, detailontwerp, deliverable-structure, design-document, documentation, template]
layer: reference
gedateerd: nee
bron: salomon-opdrachten
---

# Detailontwerp (Detailed Design) Document Skeleton

A reusable skeleton Bas applies to every detailed-design deliverable in an infrastructure engagement. Each functional area (server/application infra, virtualization, backup/restore, network) gets its own standalone Detailontwerp, and they cross-reference each other by name, version and date rather than duplicating content. The fixed structure:

- **Wijzigingsgeschiedenis (change history)**: a versioned table (author, date, description) running from 0.0.1 through client-approved 1.0.0 and beyond. Versions visibly pass through review, internal QA, client review, client comment processing, and acceptance-test updates. The version history itself is the audit trail of how the design was negotiated and accepted.
- **Inhoud (table of contents)**.
- **1 Inleiding**: context, then three fixed sub-sections: *Doel van document* (purpose), *Gerefereerde documenten* (referenced documents, as a name/subject/version-date table), *Documentopbouw* (how the rest of the document is built up).
- **2 Ontwerp**: starts with *Beschrijving toekomstige situatie* (description of the target state) and *Uitgangspunten ontwerp* (design principles/assumptions, a bullet list), then the component-by-component detail. Each component is specified with a consistent two-table pattern: a configuration table (FQDN, IP, OS, roles/features) and a specification table (CPU, memory, disks, NICs).
- **3 Implementatie- en migratieplan**: the ordered steps to build and migrate, ending in a test step.
- Where relevant, a closing **Benodigde licenties** (required licenses) list.

The deliberate moves that make this reusable: split designs per domain and let them reference each other (so each stays maintainable and a change lands in one place); always open with target-state and design principles before any detail (the reader gets the *why* before the *what*); use identical table layouts for every component (scannable, comparable, and forces completeness); and keep the change-history table as the living acceptance record.

*Bron: geanonimiseerde aanpak uit een Salomon-IT klantopdracht (a public-safety / emergency-services organization (shared emergency control-room consolidation)).*

## Verwante notities

- [Acceptance Criteria Checklist for System Delivery](acceptance-criteria-checklist.md)
- [Anatomy of a Fixed-Price Advisory Proposal](advisory-proposal-anatomy.md)
- [Functional Design with Functional Tests](functional-design-and-functional-tests.md)
- [IST/SOLL report skeleton](ist-soll-report-skeleton.md)
- [Standardize-Then-Deviate Server Provisioning](standardize-then-deviate-provisioning.md)
- [Technical/Functional Design as Cloud Blueprint](technical-functional-design-blueprint.md)
