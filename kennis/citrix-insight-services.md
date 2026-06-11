---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [insight-services, cis, troubleshooting, health-check]
layer: reference
bron: inside-citrix-fma
---

# Citrix Insight Services: automated log analysis and health checks

Citrix Insight Services (cis.citrix.com) is described by Bas as 'the glue binding it all together': you upload log and trace files and link them to support cases. It automatically analyses uploads and scans for hundreds of known issues. It reads log files from XenDesktop, XenServer, XenApp, NetScaler, PVS, ByteMobile, XenMobile, CloudBridge, CPBM and the XD/XA Connector, with more products added over time.

When it discovers known issues it suggests hotfixes, patches and updates with red/yellow/green prioritisation, analyses configuration, and gives best-practice advice with links to relevant articles/white papers. It is also useful as a quick infrastructure Health Check. Reference: CTX131233.

Call Home and CIS in Director: Citrix Call Home periodically collects system/product configuration plus performance and error info. As of XenDesktop 7.8 this can be automatically (scheduled) sent to Citrix Insight Services for proactive analysis, and CIS can be accessed instantly from Director via a drop-down menu.

## Verwante notities

- [Citrix print troubleshooting tools](citrix-print-troubleshooting-tools.md)
- [Citrix printing troubleshooting and verification tools](citrix-printing-troubleshooting-tools.md)
- [Citrix Scout: the aggregating troubleshooting tool](citrix-scout-aggregator.md)
- [Citrix Scout, TaaS and Insight Services as the 2015 troubleshooting chain](citrix-scout-taas-insight-services.md)
- [Citrix Smart Check: four building blocks and check flow](citrix-smart-check-architecture.md)
- [Citrix Smart Check: proactive Site health checks (agent or agentless)](citrix-smart-check-health-checks.md)
- [Citrix Smart Check: proactive Site health checks on top of Insight Services](citrix-smart-check-proactive-health.md)
- [Citrix's serial renaming: TaaS to Insight Services to Smart Check](citrix-taas-insight-smartcheck-naming-history.md)
- [Citrix Diagnostic Toolkit and Supportability Pack collections](citrix-toolset-collections.md)
- [Director and built-in EdgeSight](director-monitoring-tool.md)
- [Director SCOM and Insight Services integration](director-scom-and-insight-services-integration.md)
- [HDX Monitor: HDX diagnostics tool](hdx-monitor-tool.md)
