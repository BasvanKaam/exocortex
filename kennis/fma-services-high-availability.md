---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [fma, service-group, high-availability, delivery-controller, central-site-database]
layer: reference
bron: inside-citrix-fma
---

# FMA service high availability via peer service groups

Each FMA main service (a service instance) runs on every active Delivery Controller. To make them highly available, each service registers with a peer service group containing all registered service instances of the same type.

Example: with four Delivery Controllers you have four Broker services, but only one is active at a time. All four register with the Broker service group at startup, and this registration is written to the Central Site Database so all Controllers can access it. If the active Broker service fails, another takes over. There is a service group for every main FMA service (all thirteen), each with a unique identifier queryable via the PowerShell SDK.

A benefit of all services running under NT AUTHORITY\Network and using the local computer account for DB authentication: passwords are automatically changed every 30 days. Bas notes this is a big deal, since service accounts are usually very dangerous.

## Verwante notities

- [FMA architecture: Controllers, Agents and a critical central database (durable)](fma-controllers-agents-central-database.md)
- [FMA services run independently, with separate DB connection strings](fma-services-independent-registry-accounts.md)
- [FMA services: Network Service account and service isolation](fma-services-network-account-and-isolation.md)
- [FMA Zones VDA registration and Controller failover](fma-zones-vda-registration-and-failover.md)
- [The 'one is none' rule and Delivery Controller high availability](one-is-none-delivery-controller-ha.md)
- [Bas's 'one is none' rule for resilience](one-is-none-rule.md)
- [Using PowerShell to check FMA service states](powershell-fma-service-checks.md)
- [StoreFront high availability and Delivery Controller load balancing](storefront-ha-and-load-balancing.md)
