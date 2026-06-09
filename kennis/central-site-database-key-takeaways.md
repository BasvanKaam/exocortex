---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [central-site-database, key-takeaways, sql, high-availability, permissions]
layer: rich
bron: inside-citrix-fma
---

# Bas's Central Site database key takeaways

Bas's own summary list for the database chapter:

- As of XenDesktop 7.x, only Microsoft SQL is supported for the Central Site database. It contains all static and dynamic Site-wide information.
- Understand the IMA vs. FMA differences for Controllers and the database.
- For multiple geographically separated locations or multiple Zones, the Central Site database should always be in the Primary Zone / main datacenter. Even with multiple Zones it is still one central database.
- Implement some form of HA, since Connection Leasing is only a supplement.
- Delivery Controllers and the database communicate constantly; Windows authentication is required between them.
- When the database fails (even without Connection Leasing) existing connections keep working, but no new sessions and no Site-wide config changes are possible.
- Do not install SQL on the same machine as a Delivery Controller; keep the database server physically close to the Controllers.
- SQL (server or Express) must be installed before creating a Site. SQL Express is mainly for PoC/testing but can serve small production environments (no HA).
- You must be a local administrator and domain user to create/initialize databases. Required roles: dbcreator, securityadmin, db_owner. Using Studio, the account must be a sysadmin server role member.
- As of version 7.12 the LHC got renewed and re-introduced.
