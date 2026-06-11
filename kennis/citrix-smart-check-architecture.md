---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, smart-check, smart-tools, diagnostics]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Citrix Smart Check: four building blocks and check flow

Smart Check (delivered cloud-only from Citrix Cloud, but able to check on-prem or cloud XenApp/XenDesktop 7.6+) aggregates diagnostics tools into one and is best used proactively, not just for troubleshooting. It rests on four pillars:

- **Check**: human-readable name representing one or more conditions to check.
- **Collector**: a script/tool (or both) that runs checks and collects raw results.
- **Analyzer**: system that evaluates collector results and raises/lowers alerts (in 2017 the only analyzer was Citrix Insight Services).
- **Alert**: a unit of actionable information reflecting an external condition.

Flow: the backend deploys a collector blueprint to the primary Delivery Controller -> the Smart Tools agent runs it (output usually a JSON file) -> results go to the analyzer (CIS) -> backend invokes the Analysis API -> raised alerts shown in the UI.

Agentless option: by first running Citrix Scout and/or Call Home, Smart Check can discover a Site from the gathered data, but without the Site Agent it only shows Delivery Controllers and Machine Catalogs (no Delivery Groups, no scheduling, no Site details).

How it worked then in 2017.

*Bron: blogpost 'Heads up! Citrix Smart Check introduces diagnostics uploads and custom checks and alerts - deep dive (and video) included' (2017-07-31), basvankaam.com.*

## Verwante notities

- [Citrix Insight Services: automated log analysis and health checks](citrix-insight-services.md)
- [Citrix Scout, TaaS and Insight Services as the 2015 troubleshooting chain](citrix-scout-taas-insight-services.md)
- [Citrix Smart Check: proactive Site health checks (agent or agentless)](citrix-smart-check-health-checks.md)
- [Citrix Smart Check: proactive Site health checks on top of Insight Services](citrix-smart-check-proactive-health.md)
- [Citrix's serial renaming: TaaS to Insight Services to Smart Check](citrix-taas-insight-smartcheck-naming-history.md)
- [Citrix's problem is integration and focus, not lack of products](positie-citrix-should-integrate-not-just-build.md)
- [Smart Check as the future single Citrix diagnostics tool](smart-check-absorbing-cis-stance.md)
