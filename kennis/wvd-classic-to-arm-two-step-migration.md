---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [nerdio, wvd, avd, migration, arm]
layer: reference
gedateerd: ja
bron: nerdio-blog
---

# WVD Classic to ARM migration: the two-step pattern

Migrating an existing WVD Classic (non-ARM, v1 / "Fall") tenant to the WVD ARM model (v2 / "Spring") does not require a rebuild from scratch or reassigning users. Nerdio Manager for WVD handles it as a two-step process that can run as separate phases or in parallel, fully automated.

**Onboard first (associate existing deployments).** After installing Nerdio Manager, link the Resource Group and Network (vNet) where the existing WVD machines live, refresh the Tenants/Workspaces page, and the VMs appear. "Associate" them with the manager and they are under management. Applies to both old and new Tenants and Workspaces.

**Static to dynamic hostpool.** Tenants and Workspaces do not natively support advanced autoscaling. Nerdio can auto-convert a static hostpool into a dynamic one so it gains autoscaling and (auto) recovery. Can be done before or after migrating Tenants to Workspaces.

**Step one (metadata).** Select the hostpool to migrate, choose a destination Workspace, set a new hostpool name (defaults to existing), and decide what to do with user assignments: copy, move, or neither. Non-disruptive and fast.

**Step two (host VMs).** Migrate the host VMs plus all hostpool settings. Set concurrency (how many VMs at once) and the allowed number of failures before aborting. Set a schedule (time zone + window) or run immediately. Notify active sessions so users can save and log off.

**Why split the phases.** If VM migration fails, machines are not reverted to their original state and may need a rebuild. The mitigating design: step one already created a new hostpool with assignments, so VMs can be rebuilt automatically via the autoscaling engine using the same machine image (roughly 20 minutes), or with a different/updated image while reusing the migrated assignments. This is why the failure risk is described as minimal.

**Client URL change.** Once migrated, use the ARM web (HTML5) client URL: `https://rdweb.wvd.microsoft.com/arm/webclient` instead of the old non-ARM `https://rdweb.wvd.microsoft.com/webclient`.

*Bron: Nerdio-content 'Available today. How to migrate from WVD Classic (non-ARM) to WVD ARM, fully automated' (Blogs).*

## Verwante notities

- [Static vs dynamic host pools in Nerdio (autoscale eligibility)](nerdio-static-vs-dynamic-host-pools.md)
- [Hybrid WVD Object Model (NMW, Fall/Spring era)](nmw-hybrid-wvd-object-model.md)
- [WVD Spring (ARM) release: Workspaces vs Fall Tenants in NMW](nmw-spring-update-workspaces-vs-fall-tenants.md)
- [Onboarding an existing WVD deployment into Nerdio (non-disruptive)](onboarding-existing-wvd-into-nerdio-non-disruptive.md)
- [WVD Fall vs Spring release (non-ARM vs ARM)](wvd-fall-vs-spring-release.md)
- [Migrating WVD from Tenant to Workspace (ARM) in Nerdio](wvd-tenant-to-workspace-arm-migration.md)
