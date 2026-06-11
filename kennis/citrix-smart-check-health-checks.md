---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, smart-check, smart-tools, health-check, insight-services, xenapp]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Citrix Smart Check: proactive Site health checks (agent or agentless)

Smart Check (tech preview at the time, part of the Citrix Smart Tools portfolio, formerly Lifecycle Management Services) ran proactive health checks against XenApp/XenDesktop Sites. Three check categories: Site Health Checks (43+ major checks covering SQL databases, AD, Windows Firewall, hypervisor and FMA service registration, using the FMA Environment Test Services), Apps and Desktops Health Checks (verify Delivery Groups can deliver), and Update Checks (patch level of Delivery Controllers and VDAs, with hotfix recommendations). Supported on XenApp/XenDesktop 7.6 LTSR and 7.11 CR and up; not supported for the Citrix Cloud XenApp/XenDesktop Service.

Agent vs agentless: install the Smart Tools Site Agent on a Delivery Controller for full features and scheduled checks; without an agent you can run manual checks by first running Citrix Scout / Call Home and letting Smart Check discover the Site from the gathered data (Delivery Controllers and Machine Catalogs only, no Delivery Groups, StoreFront or Site DBs). Dated tech-preview product, but the proactive-health-check pattern is durable.

*Bron: blogpost 'Citrix Smart Check -- the latest addition to the Smart Tools portfolio' (2017-01-31), basvankaam.com.*

## Verwante notities

- [Citrix Call Home telemetry and how it worked](citrix-call-home-telemetry.md)
- [Citrix Insight Services: automated log analysis and health checks](citrix-insight-services.md)
- [Citrix Smart Check: four building blocks and check flow](citrix-smart-check-architecture.md)
- [Citrix Smart Check: proactive Site health checks on top of Insight Services](citrix-smart-check-proactive-health.md)
- [Citrix's serial renaming: TaaS to Insight Services to Smart Check](citrix-taas-insight-smartcheck-naming-history.md)
- [Use health-check tooling proactively, not when things fall apart](use-health-checks-proactively-not-reactively.md)
