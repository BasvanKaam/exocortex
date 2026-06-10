---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [central-site-database, configuration-logging, monitoring-database, director]
layer: reference
bron: inside-citrix-fma
---

# The three XenDesktop databases

Besides the Central Site database, XenDesktop has two more databases:

- Configuration-Logging database: stores information about all Site configuration changes and other administrative activities. Only used when the Configuration-Logging feature is enabled, which it is by default.
- Monitoring database: stores all information used by Director, such as session and connection information. Expected to grow the largest of the three.

The Central Site database itself comprises the database file (Site information, data and objects like stored procedures, tables, views) and the Transaction-Log file.

## Verwante notities

- [The Central Site database in the FMA](central-site-database-fma.md)
- [High-availability options for the Central Site database](central-site-database-ha-options.md)
- [The XenDesktop Central Site database](central-site-database-role.md)
- [Director dashboard, Trends view and alerts](director-dashboard-trends-and-alerts.md)
- [Director, EdgeSight and historical data licensing](director-edgesight-and-licensing.md)
- [Director and built-in EdgeSight](director-monitoring-tool.md)
- [FMA database sizing numbers](fma-database-sizing-numbers.md)
- [SQL Transaction-Log recovery modes for Citrix databases](sql-transaction-log-recovery-modes.md)
