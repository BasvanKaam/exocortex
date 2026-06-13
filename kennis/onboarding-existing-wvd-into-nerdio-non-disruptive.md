---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [wvd, onboarding, migration, autoscale]
layer: reference
gedateerd: ja
bron: nerdio-blog
---

# Onboarding an existing WVD deployment into Nerdio (non-disruptive)

Key reusable explainer from Bas's field experience: you do not have to start over to adopt Nerdio. Existing WVD deployments (test or production) can be reused by onboarding them into Nerdio Manager, during production hours, without users noticing.

Mechanics he describes:
- Settings > Azure environment > Link the network and resource group where WVD is deployed.
- Workspaces > refresh the page, the existing deployment appears almost instantly.
- Associate the existing Workspace or Tenant with Manager for WVD. Time depends on number of hostpools and VMs: roughly 5-15 minutes on average.

Rough timings he quotes (dated, product/version specific): NMW install 25-30 min (just wait); building a new Workspace + hostpool + a few VMs ~15 min extra; onboarding an existing environment 5-15 min.

Note: NMW (Nerdio Manager for WVD) is the legacy product name; current naming is Nerdio Manager for Enterprise (NME). Treat product names and screen labels as version-specific.

*Bron: Nerdio-content 'How to move your existing WVD deployment to a better platform NMW' (Blogs).*

## Verwante notities

- [Common WVD/Azure adoption challenges (from the field)](common-wvd-adoption-challenges.md)
- [Don't make the management tool highly available, spend the budget on compute and storage](dont-make-nerdio-manager-highly-available.md)
- [Don't Spend Budget Making the AVD Management Tool Highly Available](dont-make-the-avd-management-plane-highly-available.md)
- [Nerdio image lifecycle: import, update, re-image](nerdio-image-lifecycle-import-update-reimage.md)
- [Nerdio Manager for WVD deploys into your own Azure tenant](nerdio-manager-wvd-deploys-in-your-tenant.md)
- [NME persists machine names across reimage/rebuild](nme-hostpool-naming-persistence.md)
- [NME to NMM migration runbook (AVD)](nme-to-nmm-migration-runbook.md)
- [NME / AVD troubleshooting cheat sheet](nme-troubleshooting-cheatsheet.md)
- [NMM's four customer onboarding scenarios and what each reuses](nmm-customer-deployment-scenarios.md)
- [NMW Deployment: What to Have Ready Before You Install](nmw-deployment-prereqs-checklist.md)
- [Structure for a 45-minute 'getting started' onboarding session](nmw-getting-started-session-structure.md)
- [Hybrid WVD Object Model (NMW, Fall/Spring era)](nmw-hybrid-wvd-object-model.md)
- [Installing Nerdio Manager for WVD from the Azure Marketplace](nmw-install-from-azure-marketplace.md)
- [WVD Classic to ARM migration: the two-step pattern](wvd-classic-to-arm-two-step-migration.md)
- [Migrating WVD from Tenant to Workspace (ARM) in Nerdio](wvd-tenant-to-workspace-arm-migration.md)
