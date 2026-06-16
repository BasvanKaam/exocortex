---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [nerdio, wvd, avd, autoscale, image-management, dated]
layer: reference
gedateerd: ja
bron: nerdio-blog
---

# Hybrid WVD Object Model (NMW, Fall/Spring era)

Historical note from Bas's early Nerdio Manager for WVD writing (WVD/RDMI era, before the AVD rename). Two points worth keeping as dated reference:

- **Hybrid WVD Object Model** — Nerdio Manager could operate both the WVD Fall release and the Spring update simultaneously from one interface, and migrate Fall-to-Spring (including underlying VMs) fully graphically and automated once Microsoft gave the signal. Bas named this the 'hybride WVD Object Model.'
- **Auto-scale aggressiveness** — configurable High/Medium/Low aggressiveness driving when underlying VMs are powered on/off based on demand, with options ranging from only powering off empty machines, to notifying and logging users off, to force-shutdown on a schedule.
- **Adoption of existing environments** — existing WVD environments can be taken over by Nerdio in minutes; no need to start over.

Most of this blog's content (cost vs UX trade-off, image management simplicity, hiding complexity, the Microsoft co-development relationship) is already covered in the brain — captured here only for the dated naming and the hybrid object model term.

*Bron: Nerdio-content 'Nerdio Manager for WVD - Kosten optimalisatie, eenvoud en gebruikersvriendelijkheid' (Blogs).*

## Verwante notities

- [Nerdio Manager for WVD Community Edition (2020)](nerdio-manager-wvd-community-edition.md)
- [What the Nerdio autoscale engine does (NMW era)](nmw-autoscale-engine-capabilities.md)
- [Nerdio Manager for WVD: the cost-saving levers (WVD era)](nmw-cost-saving-levers-overview.md)
- [Onboarding an existing WVD deployment into Nerdio (non-disruptive)](onboarding-existing-wvd-into-nerdio-non-disruptive.md)
- [Hide the Complexity, Broaden the Line Between UX and Cost](position-hide-complexity-broaden-the-line.md)
- [WVD Classic to ARM migration: the two-step pattern](wvd-classic-to-arm-two-step-migration.md)
- [Migrating WVD from Tenant to Workspace (ARM) in Nerdio](wvd-tenant-to-workspace-arm-migration.md)
