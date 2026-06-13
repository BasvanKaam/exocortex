---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [nerdio, nmw, community-edition, wvd, avd, azure, tech-insider]
layer: reference
gedateerd: ja
bron: nerdio-content
---

# Nerdio Manager for WVD Community Edition (2020)

Historical product note. Nerdio Manager for WVD (NMW) Community Edition (CE) launched September 21, 2020 as part of the Nerdio Tech Insider community program. Captured for provenance; the product has since been renamed and superseded.

**How you get it:** Azure marketplace only, same as the paid version. You install the regular NMW, and once installed a banner at the top gives three choices: keep using Trial mode (for PoC and production), upgrade to paid (production workloads), or select the Community Edition (private lab only).

**The terms that mattered:**
- Free of charge, no license fees, runs until you uninstall or deactivate.
- Private Azure lab purposes ONLY. Not allowed in a company lab, not for testing/evaluating in a business context, not for production. That is what trial mode is for, and Nerdio said it would monitor this.
- Hard cap of 25 total users (also monitored).
- Full feature set, no exceptions. No limits on machine type or number of CPUs.
- Azure only. Not other clouds, not on-premises.

**Cost caveat Bas stresses:** CE is free, but you still pay for the underlying Azure resources NMW consumes, because NMW is built from Azure-native PaaS services (App Service plan, SQL database, etc.). Scale those down to keep costs minimal; an MSDN account is enough to get through the month.

**Support model:** normal support channels do not apply. Best-effort community support via the Nerdio Tech Insider Slack channel, plus the dedicated Zendesk KB page (how-to videos, troubleshooting) as the number-one go-to resource.

*Bron: Nerdio-content 'KB - Nerdio Manager for WVD Community Edition' (KB Articles).*

## Verwante notities

- [Idee: Nerdio Tech Insider Community Program](idee-nerdio-tech-insider-community-program.md)
- [Idea: a sales-free tech community feedback program](idee-nerdio-tech-insider-community-program-2.md)
- [NMW Community Edition: what it is and how to run it on a budget](nmw-community-edition-explainer.md)
- [Hybrid WVD Object Model (NMW, Fall/Spring era)](nmw-hybrid-wvd-object-model.md)
