---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [director, dashboard, trend, alerts, machine-control]
layer: reference
bron: inside-citrix-fma
---

# Director dashboard, Trends view and alerts

The default Dashboard (license-dependent) shows: connection failures, failed desktop/server OS machines, license status, currently connected sessions, average user logon duration, and infrastructure health (Delivery Controllers and any hypervisor hosts). Director uses PowerShell to monitor the main infrastructure services.

Drill down by clicking failures or statistics, or apply Filters. The Trends view accesses historical info on sessions, connection failures, machine failures, logon performance and load evaluation per site, plus hosted application usage, desktop/server/VM usage and HDX Insight network analysis. Graphical data exports to PDF, Excel or CSV.

Machine state control: start/restart/forced restart, shutdown/forced shutdown, suspend/resume, and maintenance mode. The machine details view shows installed hotfixes on the VDA.

FMA fact: as of version 7.7 Director can use integrated Windows authentication so domain-joined users access it without re-entering credentials.

Alerts: critical alerts and warnings on the main dashboard (updated every minute by default). An orange triangle means a minimum threshold was reached; a red circle means the maximum was reached. You can configure Citrix Alerts policies with email notifications and over ten policy conditions.

Director also supports different views tailored to administrative roles, with delegated administration based on administrators, roles and scopes (matching Studio).

## Verwante notities

- [Citrix Director: monitoring and troubleshooting tool](citrix-director-overview.md)
- [Director, EdgeSight and historical data licensing](director-edgesight-and-licensing.md)
- [Director and built-in EdgeSight](director-monitoring-tool.md)
- [Director SCOM and Insight Services integration](director-scom-and-insight-services-integration.md)
- [Using PowerShell to check FMA service states](powershell-fma-service-checks.md)
- [The three XenDesktop databases](xendesktop-three-databases.md)
