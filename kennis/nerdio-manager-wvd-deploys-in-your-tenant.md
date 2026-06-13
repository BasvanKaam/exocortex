---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-10
tags: [nerdio, wvd, azure, deployment, architecture]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Nerdio Manager for WVD deploys into your own Azure tenant

As of the March 2020 release, Nerdio Manager for WVD was available from the Azure Marketplace and could be spun up in any region. Key architecture point Bas calls out: it deploys within your own tenant, so you keep full control (he flags security as the reason this matters).

The deployment creates a set of Azure services in your subscription: an App Service, an Automation account, a Key Vault, an Azure SQL database, and Application Insights. His cost tip for test-drives: drop the App Service from B3 (default) to B1 (free tier won't work) and use the smallest SQL database size.

Dated to the 2020 product (the SQL-database requirement, the B3 default, the 'WVD' name before the Azure Virtual Desktop rename), but the install pattern (marketplace deploy -> outputs tab web app URL -> run the PowerShell runbook -> log in) is how the product worked then.

*Bron: blogpost 'How to: Nerdio Manager for WVD, first steps (install + first tenant)' (2020-04-14), basvankaam.com.*

## Verwante notities

- [Citrix Managed Desktop: single-bill DaaS on Citrix-managed Azure](citrix-managed-desktop-model-2019.md)
- [Nerdio Manager for WVD roadmap as of mid-2020](nerdio-2020-product-roadmap-snapshot.md)
- [Nerdio shines where Microsoft's WVD HA docs are missing](nerdio-fills-microsoft-wvd-ha-doc-gap.md)
- [Nerdio Manager for WVD launched March 2020 with fast traction](nerdio-manager-wvd-early-traction.md)
- [Nerdio innovating on top of WVD is 'a perfect marriage'](nerdio-plus-microsoft-perfect-marriage.md)
- [WVD prerequisites Nerdio still relies on: AD sync and FSLogix profiles](nerdio-wvd-prerequisites-ad-fslogix.md)
- [Nerdio Manager for WVD core capabilities circa 2020](nmw-core-capabilities-2020.md)
- [NMW Deployment: What to Have Ready Before You Install](nmw-deployment-prereqs-checklist.md)
- [Installing Nerdio Manager for WVD from the Azure Marketplace](nmw-install-from-azure-marketplace.md)
- [WVD Spring (ARM) release: Workspaces vs Fall Tenants in NMW](nmw-spring-update-workspaces-vs-fall-tenants.md)
- [Onboarding an existing WVD deployment into Nerdio (non-disruptive)](onboarding-existing-wvd-into-nerdio-non-disruptive.md)
- [WVD Fall vs Spring release (non-ARM vs ARM)](wvd-fall-vs-spring-release.md)
- [WVD technology partner ecosystem reached 13 partners (2019)](wvd-partner-ecosystem-2019.md)
