---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [nerdio, nmw, wvd, community-edition, azure-cost]
layer: reference
gedateerd: ja
bron: nerdio-blog
---

# NMW Community Edition: what it is and how to run it on a budget

Nerdio Manager for WVD (NMW) Community Edition, launched October 21, 2020 as part of the Nerdio Tech Insider community program.

What it is:
- Free of charge, but lab-only. Explicitly NOT allowed in a company lab for testing/evaluation or production; that is what trial mode is for. CE is for private Azure lab purposes only.
- Full feature set: technical differences between NMW and NMW-CE are little to none.
- Capped at 25 end-users (a monitored metric); no limit on type or number of machines/CPUs.
- Azure-only (not other clouds, not on-premises). Available exclusively via the Azure Marketplace.

How to get it: install the regular NMW from the Marketplace, then via the banner at the top choose one of three paths: keep using trial mode (PoC/production), upgrade to paid (production), or select Community Edition (private lab only). CE installs into a separate, initially empty Azure Resource Group, so it is easy to remove.

Cost discipline (his reusable point): CE is free, but you still pay for the underlying Azure resources it consumes, including the PaaS services NMW itself runs on (App Service Plan + SQL database). Keep costs minimal by scaling down that App Service Plan and SQL database; on an MSDN account that is enough to get through the month. Always set Azure cost limits and alerts on the subscription.

Support for CE is best-effort via the Tech Insider Slack channel, not normal support channels.

*Bron: Nerdio-content 'Nerdio Manager for WVD Community Edition' (Blogs).*

## Verwante notities

- [Azure cost-control habits for a test lab](azure-classic-cost-control-takeaways.md)
- [Idee: Nerdio Tech Insider Community Program](idee-nerdio-tech-insider-community-program.md)
- [Nerdio Manager for WVD Community Edition (2020)](nerdio-manager-wvd-community-edition.md)
- [Structure for a 45-minute 'getting started' onboarding session](nmw-getting-started-session-structure.md)
- [Installing Nerdio Manager for WVD from the Azure Marketplace](nmw-install-from-azure-marketplace.md)
- [NMW architecture: PaaS-only deploy, metering-only billing](nmw-paas-architecture-and-billing-model.md)
- [NMW is built for enterprise scale; small shops should look elsewhere in the portfolio](nmw-targets-enterprise-not-small-shops-position.md)
- [Cheap WVD lab: de-allocate VMs, pay only for storage](wvd-lab-cost-deallocate-vms.md)
