---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, smart-check, smart-tools, insight-services, health-checks]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Citrix Smart Check: proactive Site health checks on top of Insight Services

How it worked then (2017): Smart Check is a new cloud-based service in the Smart Tools portfolio (formerly Citrix Lifecycle Management Services) that builds on Citrix Insight Services (CIS, previously TaaS). CIS is the 'analyser / brains' that processes a collector's output and raises/lowers alerts; Smart Check is the proactive front end keeping XenApp/XenDesktop Sites healthy. Coverage at launch: Site Health Checks (50+ major checks plus dozens of sub-checks, e.g. SQL/database, AD, Windows Firewall, hypervisor, service registration), Apps & Desktops Health Checks, Update Checks, and LTSR checks. It generates separate alerts for VDI and RDS Delivery Groups, can auto-update on missing hotfixes, supports rollback, and securely uploads Site diagnostics to CIS for Citrix support. Diagnostic data is JSON that does not identify org/admins/end users. Supported on 7.6 LTSR / 7.11 CR and up, on AWS, Azure RM, XenServer 6.1/6.5/7.0, vSphere 5.1/5.5/6.0 and MCS catalogs, but not (then) on the XenApp/XenDesktop Service in Citrix Cloud. Full features need the Smart Tools Site Agent on a Delivery Controller; agentless manual checks work via Scout/Call Home discovery but exclude Delivery Groups and other components like StoreFront and Site databases. A dated product but a clean example of agent-plus-cloud-analyser proactive monitoring.

*Bron: blogpost 'Citrix Smart Check one-stop shop' (2017-05-11), basvankaam.com.*

## Verwante notities

- [Citrix Insight Services: automated log analysis and health checks](citrix-insight-services.md)
- [Citrix Smart Check: four building blocks and check flow](citrix-smart-check-architecture.md)
- [Citrix Smart Check: proactive Site health checks (agent or agentless)](citrix-smart-check-health-checks.md)
- [Citrix Lifecycle Management Services and blueprints](cwc-lifecycle-management-services.md)
- [Reboots are a necessary evil; handle them proactively](proactive-over-reactive-ops.md)
- [Smart Check as the future single Citrix diagnostics tool](smart-check-absorbing-cis-stance.md)
- [Use health-check tooling proactively, not when things fall apart](use-health-checks-proactively-not-reactively.md)
