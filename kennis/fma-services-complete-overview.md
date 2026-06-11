---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, fma, delivery-controller, broker-service, configuration-service, architecture, xendesktop]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# The FMA core services and how they communicate

How the FlexCast Management Architecture (FMA) services worked on a Delivery Controller as of XA/XD 7.12 (2016).

Communication: FMA services run isolated but talk to each other via WCF (Windows Communication Foundation) end points / service interfaces, over port 80 by default (changeable, encryption supported). Each service uses its own DB connection string to the Central Site database, so one service failing doesn't take down others (but a change like the connection string must be applied to all services). All FMA services run under NT AUTHORITY\Network service; they authenticate to the Central Site DB using the local computer account. Unlike the IMA, the FMA Delivery Controller only brokers connections to VDAs; it hosts no sessions of its own, and all ICA/HDX processing lives on the VDA.

Four services have a prominent 'core' role: Broker, Configuration, Delegated Administration, Configuration Logging.

The services:
1. Broker Service (the 'workhorse'): also houses the XML Service and STA. Handles VDA registration, connection brokering, resource enumeration, STA ticket creation/validation (only for NetScaler-launched resources), user validation, load-balancing participation, power management, SSO credential caching, idle pool management. As of 7.12 also the Principal Broker Service for LHC. The STA has been part of the Broker since Presentation Server 4.0; the XML service was rewritten in .NET into the Broker as of XenDesktop 4.x.
1.2 The Broker also houses 18 Site Services (e.g. Licensing, RebootScheduleManager, IdleSessionManager, RemotePC, PowerPolicy). Each Site service runs on only one Controller (distributed model); if a Controller misses a heartbeat (exchanged every 20s, 40s default timeout) its Site services move to another healthy Controller. Election is driven by the Central Site DB; manual assignment is possible but unsupported.
2. High Availability Service / Secondary Broker Service (NEW, LHC): takes over brokering during a DB outage.
3. Configuration Synchronisation Service (NEW, LHC): syncs config from Principal to Secondary Broker into a SQL Express LocalDB; informs Secondary Brokers of all controllers/Zones for elections.
4. Configuration Service: the 'glue' of the FMA. All services register with it on start-up, advertising their WCF endpoints and capabilities. Services query it (results cached 5 minutes; MCS/Machine Identity via Host Service cached 1 minute) to find and talk to each other. Stores config metadata, relieving AD.
4.1 It stores each registered service's AD machine SID; only listed SIDs (plus the always-allowed Network service account) may communicate. Check via Get-ConfigRegisteredServiceInstance.
5. Configuration Logging Service: logs all config changes and admin activity; can block changes if its DB is unreachable; supports a separate DB (recommended) as of 7.7.
6. Delegated Administration Service: validates permissions for all other services; site-wide changes fail if it's unavailable.
7. AD Identity Service: manages AD computer accounts for XA/XD machines.
8. Machine Creation Services (MCS): creates virtual machines only (use PVS for physical); needs a Host Connection configured in Studio.
9. Host Service: manages Host Connections to hypervisors (vSphere, XenServer, Hyper-V, Nutanix Acropolis) and clouds (AWS, Azure, CloudPlatform). 9.1 The Hypervisor Communications Library (HCL) is an abstraction layer/API used by Broker, Host and MCS so Citrix can add hypervisor/cloud support without rewriting code everywhere.
10. Environment Test Service: runs Studio-initiated site/Delivery Group/Catalog tests.
11. Monitor Service: produces alerts in Studio/Director (tells you something is wrong, not what); check status precisely via PowerShell (Get-BrokerServiceStatus, Get-ConfigServiceStatus, a Get- per service).
12. StoreFront Service: manages StoreFront from within Studio (appears twice: integral node and separate management node).
13. Analytics Service: collects analytical data for Director/Studio; feeds CEIP (enabled by default, as with Call Home).

*Bron: blogpost 'Complete FMA services overview, updated with the new 7.12 services' (2016-12-15), basvankaam.com.*

## Verwante notities

- [Check FMA service health with PowerShell, not just Director](check-fma-services-with-powershell.md)
- [Linux VDA install dependencies and ctxsetup.sh configuration](linux-vda-install-config-dependencies.md)
- [Prefer PowerShell over the GUI for Citrix FMA work](powershell-over-gui-for-citrix.md)
