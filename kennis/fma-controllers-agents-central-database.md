---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, fma, xendesktop7, architecture, delivery-controller]
layer: reference
gedateerd: nee
bron: basvankaam-blog
---

# FMA architecture: Controllers, Agents and a critical central database (durable)

The FlexCast Management Architecture is made up of Delivery Controllers and Delivery Agents. Agents are installed on every physical/virtual machine and register with the Controllers and license server; Controllers talk to a central SQL database. That database holds both configuration (Site policies, Machine Catalogs, Delivery Groups, published apps/desktops) and all live runtime data (who is connected to what, server load, connection state) used for load-balancing decisions.

Critical consequence Bas stresses: if the database is unreachable, running sessions keep working, but new sessions can't be established and configuration changes aren't possible - so build in database redundancy (SQL replication or clustering). This Controller/Agent/central-DB shape and its database-availability failure mode is the durable foundation that underpinned Citrix Virtual Apps and Desktops for years.

*Bron: blogpost 'FlexCast Management Architecture' (2013-05-28), basvankaam.com.*
