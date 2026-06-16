---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-16
tags: [citrix, workspace-cloud, citrix-cloud, daas, hybrid, fma, inside-citrix]
layer: reference
gedateerd: ja
bron: inside-citrix-book
---

# Citrix Workspace Cloud control plane and resource locations

How it worked circa 2015-2016. Citrix Workspace Cloud (CWC) was the precursor to what became Citrix Cloud. It is a management platform: Citrix runs the FMA control plane for you so you only manage the workloads.

Architecture, top to bottom:
- **Control plane (CWC control centre):** Citrix-hosted and Citrix-managed. The Delivery Controllers, SQL database, License Server, Studio, Director, and (optionally) StoreFront all live up in CWC as part of the Apps and Desktops service. The admin consoles look and feel identical to on-prem Studio and Director.
- **Resource Locations:** customer/partner-owned and controlled. This is where the VDAs, data, and applications live, plus NetScaler. Can be on-premises, in a datacentre, or on public/private cloud (Azure, AWS, Citrix CloudPlatform). You host them wherever you like.
- **Cloud Connector:** links resource locations to the CWC services.

CWC also offered Mobility Management (XenMobile), Secure Documents (ShareFile), and Lifecycle Management. New FMA features landed in CWC first (via a phased "bucket" rollout, under NDA at the time) before reaching on-prem XenApp/XenDesktop.

Bas calls it the ultimate hybrid cloud model.

*Bron: Inside Citrix (2016), 'Inside Citrix ch25 - Citrix Workspace Cloud'.*

## Verwante notities

- [Citrix Cloud Connector replaces the on-prem Delivery Controller as broker](citrix-cloud-connector-as-broker.md)
- [Citrix Lifecycle Management blueprints](citrix-lifecycle-management-blueprints.md)
- [Workspace Cloud lacked an on-prem control plane in 2015](citrix-workspace-cloud-control-plane-2015.md)
- [Citrix Workspace Cloud credential and authentication handling](citrix-workspace-cloud-credential-handling.md)
- [Citrix Workspace Cloud as the hybrid bridge](citrix-workspace-cloud-hybrid-model.md)
- [Citrix Workspace Cloud (CWC): a managed control plane over the FMA](citrix-workspace-cloud-overview.md)
- [CWC hybrid model is the way forward for Citrix](cwc-hybrid-cloud-is-the-way-forward.md)
