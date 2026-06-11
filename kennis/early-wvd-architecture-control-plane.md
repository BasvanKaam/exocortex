---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [wvd, azure, rdmi, architecture, reverse-connect]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Early WVD architecture: Microsoft-managed PaaS control plane + reverse connect

As documented March 2019 (PM-verified): WVD management runs from a central Microsoft-managed Azure control panel (PaaS), based on the RDMI technology announced in 2017. The control panel houses the Broker, Web Access, Diagnostics, the Gateway role and Load Balancing (load balancing is part of the Broker, not a separate role), all run by Microsoft. Each VM runs a WVD agent that communicates with the control panel. Reverse Connect means outbound WebSocket connections go from customer VMs to the Broker/Gateway, so no inbound ports to customer environments are needed; bidirectional VM-to-WVD traffic goes over 443. Prerequisites: valid Azure subscription, Azure AD, a Windows Server AD synced via Azure AD Connect or Azure AD DS, and a vNet that contains or connects to that AD. VMs could not be Azure AD-joined (standard or hybrid domain join only). RBAC offered Owner, Contributor, Reader and Operator roles.

How WVD worked at preview; much of this evolved into Azure Virtual Desktop, but reverse-connect-over-443 and the managed control plane remain conceptually intact.

*Bron: blogpost 'The Windows Virtual Desktop - what we know so far. 83 facts listed' (2019-03-19), basvankaam.com.*

## Verwante notities

- [Azure building blocks to extend, protect and migrate RDS/WVD](azure-services-for-rds-wvd-extend-migrate.md)
- [WVD Spring (ARM) release: Workspaces vs Fall Tenants in NMW](nmw-spring-update-workspaces-vs-fall-tenants.md)
- [Windows Server 2019 at announcement: LTSC/SAC, RDSH question, RDmi](windows-server-2019-ltsc-sac-rdmi.md)
- [WVD App Group rules (2019)](wvd-app-groups-rules-2019.md)
- [Even with managed WVD, the customer still owns the base image](wvd-customer-still-owns-the-base-image.md)
- [WVD Fall vs Spring release (non-ARM vs ARM)](wvd-fall-vs-spring-release.md)
- [WVD is what used to be RDMI](wvd-is-rdmi-on-prem-history.md)
- [WVD: what Microsoft makes HA vs what you must](wvd-managed-vs-customer-responsibility.md)
- [WVD tenant setup gotchas (2019 workshop)](wvd-tenant-setup-gotchas-2019.md)
