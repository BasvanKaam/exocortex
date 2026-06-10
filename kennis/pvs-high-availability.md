---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [citrix, pvs, high-availability, sql, replication]
layer: reference
bron: inside-citrix-fma
---

# PVS high availability

A highly available PVS environment has several components to protect:
- The PVS **SQL database**.
- Your physical or virtual **Provisioning Servers** (at least two, with HA enabled in the PVS software from the management console).
- The **storage** holding your vDisks (shared or made HA).
- The **TFTP servers** for Bootstrap delivery.

Multiple PVS servers can also load-balance streaming traffic active/active. When vDisks are stored locally on each server, you must replicate them so all servers offer identical vDisks — doable manually from the console, with recommended automation via **DFS-R** and **Robocopy**.

SQL HA options: PVS has a built-in **offline database support** mechanism (uses a snapshot when the database is unavailable; disabled by default), and Database Mirroring, SQL Clustering and SQL Always On are all valid.

## Verwante notities

- [Bas's take on application-aware HA alternatives for SQL](bas-on-application-aware-ha-alternatives.md)
- [Bas's PVS recommendation: hybrid versioning approach](bas-pvs-hybrid-versioning-recommendation.md)
- [High-availability options for the Central Site database](central-site-database-ha-options.md)
- [Bas's 'one is none' rule for resilience](one-is-none-rule.md)
- [Provisioning Services essentials and Bas's advice](provisioning-services-essentials.md)
- [Bas's PVS key takeaways and best-practice asides](provisioning-services-key-takeaways.md)
- [Citrix Provisioning Services (PVS) overview](provisioning-services-overview.md)
- [PVS boot mechanism: Bootstrap, TFTP and BDM](pvs-boot-mechanism-bootstrap-tftp-bdm.md)
- [PVS terminology: Farm, Site, Store, Device Collection, Target Device](pvs-terminology-farm-site-store-collection.md)
- [PVS vDisk creation, Standard vs Private Image Mode](pvs-vdisk-standard-vs-private-image-mode.md)
- [PVS write cache options](pvs-write-cache-options.md)
- [SQL Transaction-Log recovery modes for Citrix databases](sql-transaction-log-recovery-modes.md)
