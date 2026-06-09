---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [sql, central-site-database, high-availability, connection-leasing]
layer: reference
bron: inside-citrix-fma
---

# The Central Site database in the FMA

As of XenDesktop 7.x only SQL is supported for the Central Site database. It holds all static and dynamic Site-wide information, and even with multiple Zones it remains one central database located in the Primary Zone / main datacentre.

Key points:
- Delivery Controllers and the database communicate constantly; Windows authentication is required between them.
- When the database fails, existing connections keep working but new sessions cannot start and Site-wide configuration changes are impossible.
- Implement HA for the database; Connection Leasing is only a supplement, not a replacement.
- Required roles to create/initialize databases: dbcreator, securityadmin and db_owner; using Studio for these operations requires the sysadmin server role. You must be a local administrator and domain user.
- SQL Express is fine for PoC/testing and small production, but has no HA.
