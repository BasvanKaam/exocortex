---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [delivery-controller, fma, brokering, services, heartbeat]
layer: reference
bron: inside-citrix-fma
---

# The Delivery Controller as the heart of the FMA

FMA fact: the Delivery Controller is the heart/workhorse and centrepiece of the FMA. Responsibilities: brokers VDA sessions, verifies user credentials, plays a key role in user login, resource enumeration and launch, load-balances hosted shared desktop connections, communicates with StoreFront/Web Interface, the Host Connection (hypervisor or cloud), and the Central Site database. As of version 7.6 it also handles Connection Leasing.

It houses eleven primary FMA services (the well-known XML service is not counted, since it is not FMA-specific):
1. Analytics service
2. Broker service
3. Configuration service
4. AD Identity service
5. Configuration Logging service
6. Delegated Administration service
7. Machine Creation service
8. Host service
9. Environment Test service
10. Monitor service
11. StoreFront service

The Controller has a direct, live connection with the Central Site database, which holds all static and dynamic info. None of this is stored locally (no LHC); heartbeat messages are exchanged every 20 seconds with a TTL of 40 seconds. It also manages registered machines for availability, load balancing and power management (starting/stopping VMs); power management is for virtual machines only, not physical. It maintains/optimizes connections using Session Reliability (Common Gateway Protocol), Auto Client Reconnect, ICA Keep-Alive and workspace control.

## Verwante notities

- [Bas's distinction: authentication versus verification](authentication-vs-verification-distinction.md)
- [The Central Site database in the FMA](central-site-database-fma.md)
- [Citrix Site policies: Entitlement, Assignment, Site Access](citrix-site-policies-powershell.md)
- [Startup license and the license checkout process](citrix-startup-license-and-checkout.md)
- [Citrix Studio: the central management console](citrix-studio-overview.md)
- [Connection Leasing mechanism](connection-leasing-mechanism.md)
- [The CWC Cloud Connector](cwc-cloud-connector.md)
- [Delivery Controller as the heart of the FMA](delivery-controller-is-heart-of-fma.md)
- [Delivery Controller server sizing and supported OS](delivery-controller-sizing.md)
- [The eighteen Broker Service Site services (distributed housekeeping)](fma-broker-eighteen-site-services.md)
- [FMA Broker Service (XML/STA) and its responsibilities](fma-broker-service.md)
- [FMA architecture: Controllers, Agents and a critical central database (durable)](fma-controllers-agents-central-database.md)
- [The four most prominent FMA core services](fma-four-prominent-core-services.md)
- [FMA services run independently, with separate DB connection strings](fma-services-independent-registry-accounts.md)
- [The FlexCast Management Architecture and its thirteen core services](fma-thirteen-core-services-overview.md)
- [FMA Controllers differ fundamentally from IMA Data Collectors](fma-vs-ima-controller-differences.md)
- [The nine main FMA components and the XenDesktop Site definition](nine-main-fma-components.md)
- [The 'one is none' rule and Delivery Controller high availability](one-is-none-delivery-controller-ha.md)
