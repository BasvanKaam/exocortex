---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [local-host-cache, lhc, high-availability, principal-broker, css]
layer: reference
bron: inside-citrix-fma
---

# FMA Local Host Cache: Principal Broker, Secondary Broker (HA) and CSS

As of XenApp/XenDesktop 7.12 the Local Host Cache (LHC) was re-introduced (new to the FMA), adding services. On every Controller running 7.12+ three LHC services reside together:

- **Principal Broker Service**: when LHC is involved the Broker Service is also called this. It accepts StoreFront connection requests, talks to the Central Site database (brokering, load balancing) and continuously interacts with the CSS and the High Availability Service.
- **High Availability Service / Secondary Broker Service**: when an outage occurs, the Principal Broker loses contact with the Central Site database, stops listening, and instructs the HA Service to start listening for incoming requests. A VDA re-registration is triggered so the HA service gets current session info. When the DB connection is restored, the Principal Broker resumes and tells the HA service to stop. The HA service then removes remaining VDA registrations and keeps updating the local SQL Express database (with CSS help).
- **Configuration Synchronisation Service (CSS)**: every two minutes it checks the Principal Broker for configuration changes and synchronises them to the HA Service. Synced data (published icons, Delivery Group/Catalog changes, certain Citrix policies) is stored in a Microsoft SQL Server Express LocalDB database on the same Controller, which is fully re-created each sync. It does NOT include current state (who is connected where). The CSS also informs each HA service about all other Controllers in the Site/zones (via an alphabetical FQDN list) to elect which Controller takes over per zone when LHC activates.

## Verwante notities

- [Connection Leasing failover behavior and limitations](connection-leasing-failover-behavior.md)
- [Connection Leasing mechanism](connection-leasing-mechanism.md)
- [FMA architectural casualties: Zones, LHC and Worker Groups removed then re-added](fma-architectural-changes-zones-lhc-removed.md)
- [Local Host Cache in XenApp 6.5 (IMA)](local-host-cache-ima.md)
- [VDA high-availability mode (direct ICA, last resort)](vda-high-availability-mode.md)
- [Zones in the FMA are not the same as IMA 6.5 Zones](zones-fma-vs-ima.md)
