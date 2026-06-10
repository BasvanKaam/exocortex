---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [site-services, broker-service, heartbeat, housekeeping, distributed]
layer: reference
bron: inside-citrix-fma
---

# The eighteen Broker Service Site services (distributed housekeeping)

The Broker Service houses eighteen so-called Site services that provide Site-wide maintenance and housekeeping (managing Host Connections, checking session idle times, reboot schedules, cache maintenance, etc.).

Each individual Site service runs on only one Delivery Controller at a time, creating a distributed model. When a Controller misses a heartbeat with the Central Site database, all its Site services transfer to another healthy Controller (from one Broker Service to another). A heartbeat is exchanged every 20 seconds with a default timeout of 40 seconds.

Site services are the exception to the rule of keeping all Controllers equally configured. At runtime they are automatically divided among active Controllers; the election is controlled by the contents of the Central Site database. You can assign Site services manually, but that is not recommended or supported.

The eighteen: ControllerReaper, ControllerNameCacheRefresh, Licensing, BrokerReaper, RegistrationHardening, WorkerNameCacheRefresh, AccountNameCacheRefresh, PowerPolicy, GroupUsage, AddressNameResolver, RebootScheduleManager, RebootCycleManager, ScopeNamesRefresh, FeatureChecks, RemotePC, IdleSessionManager, LeaseReaper, Hypervisor connection.

The **Hypervisor Connection Site service** is special: it is the only Site service that can exist on multiple Controllers in the same Site and can be configured via the PowerShell SDK. It manages Host Connections and lets you control which Controller owns a Host Connection (or they are automatically load balanced by default).

## Verwante notities

- [Broker service, XML/STA and the 18 site services](broker-service-xml-sta-site-services.md)
- [Citrix Host Connection](citrix-host-connection.md)
- [The Delivery Controller as the heart of the FMA](delivery-controller-heart-of-fma.md)
- [FMA Broker Service (XML/STA) and its responsibilities](fma-broker-service.md)
- [The four most prominent FMA core services](fma-four-prominent-core-services.md)
- [The FlexCast Management Architecture and its thirteen core services](fma-thirteen-core-services-overview.md)
