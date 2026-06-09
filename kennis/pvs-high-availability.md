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
