---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [citrix-director, edgesight, licensing, platinum, netscaler, data-retention]
layer: reference
bron: inside-citrix-fma
---

# Director, EdgeSight and historical data licensing

Director uses Citrix EdgeSight technology, now an integral part of Director (latest standalone version was 5.4). EdgeSight was powerful but complex; Director now covers roughly 80-90% of first- and second-line support tasks and is much easier to navigate. Citrix reused and rewrote part of the original EdgeSight code, focused on reporting.

EdgeSight EOL was set to 30-June-18 or 24-Aug-2016 depending on valid software maintenance / Subscription Advantage (EOM 31-Dec-17 or 24-Feb-2016).

Historical data retention by license:
- All editions: free Director troubleshooting and real-time monitoring, data stored up to 7 days (then groomed).
- XenDesktop 7.x Platinum: adds performance management and historical monitoring up to a full year, stored in the Configuration Logging database, groomed at 90-day intervals by default (configurable up to 367 days via Set-MonitorConfiguration PowerShell).
- Platinum + NetScaler Enterprise: adds network analysis plus 60 minutes of data storage max.
- Platinum + NetScaler Platinum: same plus unlimited data storage (officially supported/tested up to three years).

The Monitor Service OData API lets you build custom reports, e.g. letting Excel communicate directly with the Delivery Controller via the OData protocol.

## Verwante notities

- [Citrix Director: monitoring and troubleshooting tool](citrix-director-overview.md)
- [Director dashboard, Trends view and alerts](director-dashboard-trends-and-alerts.md)
- [Director and built-in EdgeSight](director-monitoring-tool.md)
- [Director SCOM and Insight Services integration](director-scom-and-insight-services-integration.md)
- [The three XenDesktop databases](xendesktop-three-databases.md)
