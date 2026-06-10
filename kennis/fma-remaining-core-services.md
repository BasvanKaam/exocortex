---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [fma, host-service, delegated-administration, monitor-service, analytics]
layer: reference
bron: inside-citrix-fma
---

# Remaining FMA services: Logging, Delegated Admin, AD Identity, Host, and more

- **Configuration Logging Service**: logs all configuration changes and Administrator activity in a Site. Depending on config, no Site changes are possible when its database is unreachable (one of the four core services). Data can live in the Central Site Database or, recommended, a separate database (selectable during install as of XenDesktop 7.7).
- **Delegated Administration Service**: all services consult it to validate they have the proper permissions/rights to change the Central Site Database; it manages delegated administrative permissions. If unavailable, site-wide config changes are impossible.
- **AD Identity Service**: handles all Active Directory computer accounts for XenApp/XenDesktop machines.
- **Machine Creation Services**: creates new VMs; if unavailable no new VMs can be created via MCS (and MCS only creates virtual, not physical).
- **Host Service**: manages connections between physical hosts, Delivery Controllers and the underlying hypervisor(s)/cloud platform(s), collectively 'Host Connections'. Supported hypervisors: vSphere, XenServer, Hyper-V, Nutanix Acropolis. Supported clouds: Amazon Web Services, Microsoft Azure, CloudPlatform.
- **Environment Test Service**: runs Site-wide tests from Studio (Delivery Groups, Machine Catalogs, whole Site).
- **Monitor Service**: monitors the FMA and raises alerts/warnings in Studio or Director (but tells you something is wrong, not what or where).
- **StoreFront Service**: manages your StoreFront deployment from Studio.
- **Analytics Service**: collects analytical data for Director/Studio; leveraged by CEIP and Citrix Call Home (enabled by default, data shared anonymously and encrypted).

## Verwante notities

- [The FlexCast Management Architecture and its thirteen core services](fma-thirteen-core-services-overview.md)
