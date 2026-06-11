---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [azure, rds, wvd, asr, migration, dr]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Azure building blocks to extend, protect and migrate RDS/WVD

The 2019 toolkit Bas laid out for combining on-prem RDS, Azure IaaS RDS and WVD:

- Connectivity first: Site-to-Site VPN via an Azure VPN gateway (ExpressRoute optional but pricier and often overkill).
- Identity: Azure AD needed for WVD auth; hosts must be domain-joined to Windows Server AD; keep Azure AD synced via Azure AD Connect. WVD VMs cannot be directly Azure AD joined.
- DNS: configure per-vNet or per-NIC, or stand up an additional Azure-side Domain Controller with DNS near your RDS hosts to cut DC-to-host chatter.
- DR/migration: Azure Site Recovery (ASR) for both DR and migration. Per Microsoft, migration uses the same steps as DR except failover from on-prem is the final step and you can't fail back. ASR plus Azure Traffic Manager can combine on-prem RDS with Azure IaaS RDS.
- Cost controls: Start/Stop VMs during off-hours (Azure Automation), per-VM auto-shutdown (note: no auto power-on counterpart).
- Migrate IaaS RDS to WVD: register to WVD, create tenant, create hostpool, install WVD agent on the Azure RDS machines, the agent self-registers with the WVD control panel.

*Bron: blogpost 'Combine WVD, IaaS RDS, on-prem RDS to scale, protect & migrate' (2019-04-29), basvankaam.com.*

## Verwante notities

- [Azure forced Microsoft's OS and application templates (2013)](azure-os-application-templates-2013.md)
- [Durable barriers to public cloud adoption](barriers-to-public-cloud-adoption-2016.md)
- [Early WVD architecture: Microsoft-managed PaaS control plane + reverse connect](early-wvd-architecture-control-plane.md)
- [WVD prerequisites Nerdio still relies on: AD sync and FSLogix profiles](nerdio-wvd-prerequisites-ad-fslogix.md)
- [Positie: deploying XenDesktop 7 on Azure was a waste of money in 2013](positie-xd7-on-azure-waste-of-money-2013.md)
- [WVD is what used to be RDMI](wvd-is-rdmi-on-prem-history.md)
- [WVD tenant setup gotchas (2019 workshop)](wvd-tenant-setup-gotchas-2019.md)
