---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [director, edgesight, monitoring, scom, insight-services]
layer: reference
bron: inside-citrix-fma
---

# Director and built-in EdgeSight

Director is a real-time, web-based monitoring and troubleshooting tool. Citrix EdgeSight (historical data, trends, analyses) is now built into Director and no longer sold separately; the last standalone EdgeSight was 5.4. Built-in historical reporting needs Platinum XenDesktop/XenApp licenses; network analysis needs at least NetScaler Enterprise or Platinum. Data retention depends on license: non-Platinum keeps data up to 7 days, Platinum up to a year (default 90 days).

Director offers role-based delegated administration views, shows alerts/notifications on the dashboard, and monitors the main infrastructural services (using PowerShell). It can show SCOM alerts (Citrix acquired the SCOM Comtrade management packs, and the SCOM web interface launches from Director's Alerts page) and Insight Services (fuelled by Scout and Citrix Call Home; also at cis.citrix.com). As of 7.7 it supports integrated Windows authentication. Director also works with older IMA XenApp 6.5 environments (shadow sessions, machine details, HDX panel, delegated administration, Activity Manager). See CTX139382 for best practices.

## Verwante notities

- [Check FMA service health with PowerShell, not just Director](check-fma-services-with-powershell.md)
- [The Citrix XenDesktop/XenApp 7.x troubleshooting toolset](citrix-7x-troubleshooting-toolset.md)
- [Citrix Director: monitoring and troubleshooting tool](citrix-director-overview.md)
- [Citrix Insight Services: automated log analysis and health checks](citrix-insight-services.md)
- [Citrix Scout: the aggregating troubleshooting tool](citrix-scout-aggregator.md)
- [Director dashboard, Trends view and alerts](director-dashboard-trends-and-alerts.md)
- [Director, EdgeSight and historical data licensing](director-edgesight-and-licensing.md)
- [Director SCOM and Insight Services integration](director-scom-and-insight-services-integration.md)
- [HDX Monitor: HDX diagnostics tool](hdx-monitor-tool.md)
- [Prefer PowerShell over the GUI for Citrix FMA work](powershell-over-gui-for-citrix.md)
- [VMTurbo: control the datacenter, don't just monitor it](vmturbo-control-not-monitor.md)
- [The three XenDesktop databases](xendesktop-three-databases.md)
