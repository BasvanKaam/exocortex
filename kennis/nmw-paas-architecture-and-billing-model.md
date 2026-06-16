---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [nerdio, nmw, wvd, paas, azure, architecture, billing]
layer: reference
gedateerd: ja
bron: nerdio-blog
---

# NMW architecture: PaaS-only deploy, metering-only billing

Durable design facts about how Nerdio Manager for WVD is built and billed (WVD era). Specific euro/dollar figures intentionally omitted; capture the model, not the numbers.

## Install and footprint
- Installed only via the Azure Marketplace; it is an Azure application, 100% PaaS, no VMs.
- Deploys into the customer's own Tenant/Subscription. Creates: App Service, App Service Plan, Azure SQL Database, Application Insights, Key Vault, Storage Accounts, Automation Account, Runbook.
- The install account is used once and is not stored or cached afterwards; a temporary account that you delete later works fine.
- PowerShell install path avoids having to disable MFA/conditional access for the install.

## Why PaaS (design rationale)
- Security: deployed directly into the customer's environment, private to them, no Nerdio access unless explicitly granted.
- Flexibility: PaaS scales up/down easily and speeds product development. Multiple subscriptions per tenant supported.
- Scale: default plan tier is sized to manage tens of thousands of machines; you can scale the plans down, but undersizing can hurt console responsiveness and automated actions.

## Billing and metering model
- Two license models: per-named-user and per-concurrent-user, billed on the monthly maximum unique users (de-duplicated across host pools). You can switch model month to month.
- Each month (~1st) the system inventories unique assigned/connected users and that becomes the billed license count, billed through Azure (preferably via a partner).
- Privacy: only a limited amount of metering data goes back to Nerdio. No usernames, session info, or host names.
- A separate per-host-pool compute/storage estimate shows min/max monthly Azure compute and storage cost as you change VM type, OS disk, or capacity (Azure resource cost only, not license cost).

*Bron: Nerdio-content 'FULL disclosure! Nerdio Manager for WVD costs, and licensing' (Blogs).*

## Verwante notities

- [Named vs concurrent user licensing, and the 30-day peak rule](named-vs-concurrent-user-licensing-avd.md)
- [Nerdio consumption-based licensing model](nerdio-licensing-model.md)
- [NMM architecture: native Azure PaaS deployed into the MSP's own tenant](nmm-architecture-paas-in-msp-tenant.md)
- [NMW Community Edition: what it is and how to run it on a budget](nmw-community-edition-explainer.md)
- [NMW Deployment: What to Have Ready Before You Install](nmw-deployment-prereqs-checklist.md)
- [Installing Nerdio Manager for WVD from the Azure Marketplace](nmw-install-from-azure-marketplace.md)
- [NMW is built for enterprise scale; small shops should look elsewhere in the portfolio](nmw-targets-enterprise-not-small-shops-position.md)
- [Don't hide costs from customers: full-disclosure pricing builds trust](radical-pricing-transparency-position.md)
