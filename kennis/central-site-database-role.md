---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [central-site-database, fma, sql, delivery-controller, high-availability]
layer: reference
bron: inside-citrix-fma
---

# The XenDesktop Central Site database

The XenDesktop Central Site Database holds all Site-wide static information (policies, configured Catalogs and Delivery Groups, Host Connections, Zones, etc.) as well as dynamic run-time information (who is logged on to which VDA, what resources are in use, etc.). This data is needed during user logon, authentication, resource enumeration and the actual resource launch sequence (load balancing).

It is a critical part of the infrastructure: when it is down, users cannot connect or launch resources and IT cannot make configuration changes to the Site. Some form of high-availability mechanism is therefore needed to minimize downtime. Connection Leasing helps keep certain resources available even when the database is offline.

In the FMA, Virtual Delivery Agents only communicate with the Site Delivery Controller(s); they do not access the Site database directly.

## Verwante notities

- [Delivery Controller as the heart of the FMA](delivery-controller-is-heart-of-fma.md)
- [Delivery Controller server sizing and supported OS](delivery-controller-sizing.md)
- [Delivery Controller vs Data Collector differences](delivery-controller-vs-data-collector.md)
- [FMA Zones: architecture and purpose](fma-zones-architecture-and-purpose.md)
- [The nine main FMA components and the XenDesktop Site definition](nine-main-fma-components.md)
- [SQL Transaction-Log recovery modes for Citrix databases](sql-transaction-log-recovery-modes.md)
- [The three XenDesktop databases](xendesktop-three-databases.md)
