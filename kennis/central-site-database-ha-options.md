---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [sql, high-availability, alwayson, mirroring, clustering, central-site-database]
layer: reference
bron: inside-citrix-fma
---

# High-availability options for the Central Site database

Back up the Site database regularly (daily). For HA:

- SQL Server AlwaysOn Availability Groups (recommended with SQL Server 2012 Enterprise or later): an HA/DR solution first introduced in SQL Server 2012; requires SQL instances on Windows Server Failover Clustering (WSFC) nodes.
- SQL Mirroring (recommended when AlwaysOn isn't possible): automatic failover in seconds; users generally unaffected. Requires full SQL Server licenses on each database server. SQL Express cannot be mirrored.
- SQL Clustering (third choice): more complex to set up and typically slower failover than mirroring. SQL Express does not support clustering out of the box.

Supported SQL Server versions: SQL Server 2014 (Express/Standard/Enterprise); SQL Server 2012 SP1/SP2 (Express/Standard/Enterprise; SP2 Express is installed by default with the Controller if no supported SQL is detected); SQL Server 2008 R2 SP2 (Express/Standard/Enterprise/Datacenter).

Combine HA with regular backups and a SQL Maintenance Plan to keep the database optimized, backed up and free of inconsistencies.

## Verwante notities

- [Azure Availability Sets vs Availability Zones](azure-availability-sets-vs-zones.md)
- [Bas's take on application-aware HA alternatives for SQL](bas-on-application-aware-ha-alternatives.md)
- [Connection Leasing failover behavior and limitations](connection-leasing-failover-behavior.md)
- [FMA architecture: Controllers, Agents and a critical central database (durable)](fma-controllers-agents-central-database.md)
- [MSCS Cluster Building Blocks](mscs-cluster-building-blocks.md)
- [The 'one is none' rule and Delivery Controller high availability](one-is-none-delivery-controller-ha.md)
- [Bas's 'one is none' rule for resilience](one-is-none-rule.md)
- [PVS high availability](pvs-high-availability.md)
- [SQL Server 2005 Database Mirroring with a Witness](sql-2005-database-mirroring.md)
- [SQL Server 2008 Feature Highlights](sql-server-2008-feature-highlights.md)
- [SQL Transaction-Log recovery modes for Citrix databases](sql-transaction-log-recovery-modes.md)
- [The three XenDesktop databases](xendesktop-three-databases.md)
- [Zone connection quality limits (bandwidth and RTT)](zone-connection-quality-limits.md)
