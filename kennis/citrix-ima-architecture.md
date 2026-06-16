---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [citrix, ima, data-store, local-host-cache, reference, obsolete]
layer: reference
gedateerd: ja
bron: core-knowledge-docs
---

# Citrix IMA Architecture: Data Store and Local Host Cache

The Independent Management Architecture (IMA) underpinning Presentation Server/XenApp:

- **IMA service**: runs on every Presentation Server (PS) and handles server-to-server communication.
- **IMA protocol**: the transport for that server-to-server data (port 2512).
- **IMA data store**: holds mostly static data — published applications, configuration (Citrix policies), SpeedScreen, animation settings.
- **Local Host Cache (LHC)**: each PS holds a local cache, filled from the data store at IMA service start and by default every 30 minutes. This gives redundancy and speed for data-store queries.

A farm keeps running without the data store and accepts new connections, but the management console needs a live connection to the data store to open — so configuration changes are impossible while the store is down. The data store can be replicated across multiple PS servers for redundancy and speed; if a server can reach a replica, the console can still open and make changes.

Licenses now live on a separate license server; earlier they were stored in the IMA data store.

*Bron: Core Knowledge doc 'Citrix General Core Doc' (Bas zijn vroege sysadmin-naslag).*

## Verwante notities

- [Citrix Data Collector Elections](citrix-data-collector-elections.md)
- [Citrix policy precedence: IMA vs Citrix AD vs normal AD policies](citrix-policy-precedence-ima-ad.md)
- [Citrix Presentation Server Command-Line Tools](citrix-presentation-server-cli-tools.md)
- [Citrix Server, Farm and Zone Design Trade-offs](citrix-server-farm-zone-design.md)
- [Citrix XenApp Lineage and Client Types](citrix-xenapp-lineage-and-clients.md)
- [Citrix Zones and Data Collectors](citrix-zones-and-data-collectors.md)
- [Connection Leasing is not Local Host Cache, and it's not HA](cl-is-not-lhc-and-not-ha.md)
- [Delivery Controller vs Data Collector differences](delivery-controller-vs-data-collector.md)
- [Delivery Controller vs. Data Collector (FMA vs. IMA)](delivery-controller-vs-data-collector-2.md)
- [XenApp migration tooling: Migration Center and 6.0-to-6.5 Upgrade Utility (2013)](xenapp-migration-tooling-2013.md)
