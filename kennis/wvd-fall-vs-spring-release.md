---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [wvd, azure, arm, nerdio]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# WVD Fall vs Spring release (non-ARM vs ARM)

How it worked in 2020: Windows Virtual Desktop existed in two generations. The Fall release was the original, non-ARM model based on Tenants and host pools. The Spring release moved WVD onto Azure Resource Manager (ARM), unlocking a far larger feature set. Tenants and their host pools were Fall-era; Workspaces were the Spring/ARM construct.

Migration path: Fall-to-Spring migration meant moving Tenants and host pools into a Workspace, carrying user assignments along. Nerdio Manager for WVD had this automated through a GUI, but the fully native PowerShell-module-driven path was still "coming soon" pending Microsoft's official release of the modules.

Dated marker: ARM is now the only model and "Fall/Spring release" terminology is gone. This captures the transition era.

*Bron: blogpost 'Add existing WVD deployments, migrate to ARM, and enable autoscaling' (2020-08-19), basvankaam.com.*

## Verwante notities

- [Bet: WVD third-party vendors are where the action is](betting-on-wvd-third-party-tooling-2020.md)
- [Early WVD architecture: Microsoft-managed PaaS control plane + reverse connect](early-wvd-architecture-control-plane.md)
- [Nerdio Manager for WVD roadmap as of mid-2020](nerdio-2020-product-roadmap-snapshot.md)
- [How Nerdio's WVD autoscale worked: triggers, base/burst capacity, graceful drain](nerdio-autoscale-mechanics-2020.md)
- [Nerdio Manager for WVD deploys into your own Azure tenant](nerdio-manager-wvd-deploys-in-your-tenant.md)
- [WVD Spring (ARM) release: Workspaces vs Fall Tenants in NMW](nmw-spring-update-workspaces-vs-fall-tenants.md)
- [WVD Classic to ARM migration: the two-step pattern](wvd-classic-to-arm-two-step-migration.md)
- [WVD roadmap signals from the 2019 workshop](wvd-roadmap-signals-2019.md)
- [WVD tenant setup gotchas (2019 workshop)](wvd-tenant-setup-gotchas-2019.md)
