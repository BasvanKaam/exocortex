---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-11
tags: [template, provisioning, standardization, naming-convention, best-practice, consulting-tool]
layer: reference
gedateerd: nee
bron: salomon-opdrachten
---

# Standardize-Then-Deviate Server Provisioning

Bas's standard build method for rolling out an estate of servers, stated plainly in his implementation plans: configuration is based on vendor best practices *plus our own experience from previous client engagements*, servers are first deployed from a standard template, and only then adjusted per role and function.

The pattern:

- **One standard template, then role-specific deltas.** Every server starts identical (from a template); each then gets the minimum changes its role requires. The implementation plan literally repeats "create the VM from the standard server template; install and configure for role X" for each role, which keeps the build predictable and auditable.
- **Sizing comes from two sources combined**: the product vendor's minimum requirements *and* experience from prior engagements. Not vendor minimums alone, not gut feel alone.
- **Defensive default extras baked into the template** rather than added ad hoc - e.g. every server gets a second disk reserved up front (used later for dump files), so the standard already anticipates future need.
- **A naming convention is defined before anything is built**, encoding node, type and sequence number, with cluster members sharing a number and clusters getting their own marker. Naming is a design artifact, not an afterthought.
- **Template-level hygiene** for virtual machines is standardized too (remove the floppy drive, use the paravirtual SCSI controller, use the VMXNET3 adapter, optimize BIOS for virtual use) - applied once to the template, inherited by all.

The generalizable principle: standardize the 80% in a template, deviate only for the documented 20%, and bake in your accumulated field experience as defaults so each engagement starts smarter than the last.

*Bron: geanonimiseerde aanpak uit een Salomon-IT klantopdracht (a public-safety / emergency-services organization (shared emergency control-room consolidation)).*

## Verwante notities

- [Detailontwerp (Detailed Design) Document Skeleton](detailontwerp-document-skeleton.md)
- [Fault-Tolerance Decision Hierarchy (Application HA Before Hypervisor HA)](fault-tolerance-decision-hierarchy.md)
- [Inspecting prerequisites up front saves the whole deployment](prerequisites-discipline-saves-time.md)
- [Technical/Functional Design as Cloud Blueprint](technical-functional-design-blueprint.md)
- [Principles I apply on transformation engagements](transformation-principles-positions.md)
- [Two-scenario advice and recommendation principles](two-scenario-advice-and-recommendation-principles.md)
