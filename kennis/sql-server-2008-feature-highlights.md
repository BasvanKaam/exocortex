---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [sql-server, database, reference, sql-2008]
layer: reference
gedateerd: ja
bron: core-knowledge-docs
---

# SQL Server 2008 Feature Highlights

Reference note on what SQL Server 2008 added over earlier versions, from the era when this was current.

- Policy-based management, including querying multiple servers at once.
- Data Collector for gathering management data.
- SQL Server 2008 Reporting Services.
- Scalability: row- and page-level compression, plus backup compression.
- Resource Governor: run multiple workloads on one server with scalable shares (more for one, less for another).
- Performance: locks kept low; faster queries on partitioned tables.
- Improved database mirroring, with data compressed before sending.
- Hot-add CPU on 64-bit Itanium systems using SQL Server 2008 Enterprise Edition.
- Security: encryption keys can be stored inside or outside the database.
- Development: sparse columns (columns without an added value no longer take physical disk space); several new data types.

For SQL 2000 and 2005, Bas's original notes pointed to saved web pages rather than distilling the details.

*Bron: Core Knowledge doc 'SQL 2000, 2005 and 2008 Core Doc' (Bas zijn vroege sysadmin-naslag).*

## Verwante notities

- [High-availability options for the Central Site database](central-site-database-ha-options.md)
- [SQL Server 2005 Database Mirroring with a Witness](sql-2005-database-mirroring.md)
- [SQL Transaction-Log recovery modes for Citrix databases](sql-transaction-log-recovery-modes.md)
- [SQL HA options for the XenDesktop Site database and when each fits](xendesktop-sql-ha-options.md)
