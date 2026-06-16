---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, xenapp, xendesktop, local-host-cache, fma, high-availability, broker-service]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# How Local Host Cache works in the FMA

How the re-introduced Local Host Cache (LHC) worked as of XenApp/XenDesktop 7.12 (2016), rebuilt from the ground up for the FlexCast Management Architecture (the old 6.5 LHC was a different design):

Purpose: LHC keeps site-wide brokering of new and existing connections working when a Delivery Controller loses its link to the Central Site Database, or the DB fails. Works on-premises and for Citrix Cloud, where the Cloud Connector replaces the on-prem Delivery Controller (so the LHC services live on the Cloud Connectors too).

Three services on each Controller/Connector:
- Principal Broker Service: the normal Broker Service (also XML Service and STA) when LHC is involved. Accepts StoreFront requests, brokers and load-balances against the Central Site DB.
- Configuration Synchroniser Service (CSS): every 2 minutes checks the Principal Broker for config changes and syncs them to the High Availability Service. Synced config (published icons, Delivery Group/Catalog changes, certain policies) is stored in a SQL Server Express LocalDB on the same Controller, fully re-created on each sync. The local SQL Express DB has shipped with XA/XD since 7.9. Current session/load-balancing state is NOT synced.
- High Availability Service / Secondary Broker Service: takes over when an outage occurs.

Failover flow: on outage the Principal Broker stops listening and tells the Secondary Broker to start. VDAs re-register with the Secondary Broker (which gathers current session info). When the DB connection is restored, the Principal Broker resumes, VDAs re-register back, the Secondary Broker drops remaining registrations.

Zones / multiple controllers: the CSS tells each Secondary Broker about all other controllers (incl. additional Zones). An election based on an alphabetical list of machine FQDNs decides which Controller's Secondary Broker takes over per Zone.

Sizing/limits: LocalDB can use up to 1.2 GB RAM, the HA Service up to 1 GB if LHC stays active a while; plan extra RAM, CPU and disk. At 10 logons/sec the DB grows ~1 MB every 2-3 minutes; space is reclaimed when normal operations resume. One Controller handles all connections during an outage, so its CPU runs higher than usual.

Scope: supported for server-hosted apps/desktops and static (assigned) desktops, NOT for pooled VDI desktops. Validated to manage 5000 VDAs.

LHC vs Connection Leasing (CL): always one or the other, never both. On upgrade/install with >5000 VDAs, LHC stays disabled regardless. With <5000 VDAs, whichever of CL/LHC was relevant is preserved: enable via PowerShell with Set-BrokerSite -LocalHostCacheEnabled $true -ConnectionLeasingEnabled $false.

*Bron: blogpost 'Local Host Cache returns in XenApp/XenDesktop 7.12, rebuilt for the FMA' (2016-12-05), basvankaam.com.*

## Verwante notities

- [The Broker Service bundles brokering, XML and STA in one process](citrix-broker-service-three-roles.md)
- [Connection Leasing is not Local Host Cache, and it's not HA](cl-is-not-lhc-and-not-ha.md)
- [How Connection Leasing worked in XenApp 7.6](connection-leasing-how-it-works.md)
- [FMA architecture: Controllers, Agents and a critical central database (durable)](fma-controllers-agents-central-database.md)
- [FMA Local Host Cache: Principal Broker, Secondary Broker (HA) and CSS](fma-local-host-cache-services.md)
- [Why the FMA Site database is a single point of failure (no Local Host Cache)](fma-no-local-host-cache-db-dependency.md)
- [FMA dropped zones and Local Host Cache](fma-no-zones-no-lhc.md)
- [Use LHC over Connection Leasing, and the FMA's modularity proves itself](lhc-over-connection-leasing.md)
- [Local Host Cache in XenApp 6.5 (IMA)](local-host-cache-ima.md)
- [Losing Local Host Cache was a real FMA regression](no-local-host-cache-fma-drawback.md)
- [VDA high-availability mode for Controller outages](xd7-vda-high-availability-mode.md)
- [Zone VDA registration and failover behaviour (7.7)](zones-vda-registration-failover.md)
