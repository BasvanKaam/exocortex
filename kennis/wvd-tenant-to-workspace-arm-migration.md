---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [wvd, arm, migration, host-pool]
layer: reference
gedateerd: ja
bron: nerdio-blog
---

# Migrating WVD from Tenant to Workspace (ARM) in Nerdio

Background (dated, legacy WVD): WVD came in two flavours, the old non-ARM Tenant model and the new ARM model based on Workspaces. Nerdio automated the migration from Tenants to Workspaces.

Flow Bas describes:
- Tenants section > Migrate to ARM.
- Select the hostpool (part of Tenants) and the target Workspace, and decide what to do with current user assignments. This is essentially hostpool metadata migration, takes a few seconds.
- Optionally migrate the underlying VMs (toggle Migrate VMs On). You configure: how many VMs migrate at the same time, the number of allowed failures before the process halts, a schedule (e.g. night-time) or run immediately, and a messaging template (active sessions get notified, then after a configurable delay the migration runs).
- After completion the hostpool appears under Workspaces instead of Tenants.

This whole Tenant/ARM-migration topic is largely historical now that WVD/AVD is ARM-only. Keep as background, not current guidance.

*Bron: Nerdio-content 'How to move your existing WVD deployment to a better platform NMW' (Blogs).*

## Verwante notities

- [Early WVD architecture: Microsoft-managed PaaS control plane + reverse connect](early-wvd-architecture-control-plane.md)
- [Nerdio Manager for WVD launched March 2020 with fast traction](nerdio-manager-wvd-early-traction.md)
- [NME to NMM migration runbook (AVD)](nme-to-nmm-migration-runbook.md)
- [Nerdio Manager for WVD core capabilities circa 2020](nmw-core-capabilities-2020.md)
- [Hybrid WVD Object Model (NMW, Fall/Spring era)](nmw-hybrid-wvd-object-model.md)
- [Onboarding an existing WVD deployment into Nerdio (non-disruptive)](onboarding-existing-wvd-into-nerdio-non-disruptive.md)
- [WVD Classic to ARM migration: the two-step pattern](wvd-classic-to-arm-two-step-migration.md)
