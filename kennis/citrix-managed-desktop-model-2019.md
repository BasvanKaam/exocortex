---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, managed-desktop, daas, azure, cloud, synergy-2019]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Citrix Managed Desktop: single-bill DaaS on Citrix-managed Azure

As announced at Synergy 2019 (a.k.a. Citrix DaaS). You buy everything from Citrix in one specified bill: the DaaS service plus the Azure compute to run the machines. Monthly subscription or 1-to-5-year term-based consumption; main service started at $16/user/month with a 25-user minimum, plus a pre-paid Azure consumption commitment of $5/user/month forming a pool of funds.

Architecture: VDAs and Cloud Connectors are deployed into an Azure subscription and tenant that Citrix manages (not your own subscription). Citrix ensures tenant isolation (each customer gets their own subscription + AAD), audits its own access, and is wholly responsible for the non-domain-joined Cloud Connectors. There is nothing for the customer to maintain architecturally (Delivery Controllers, Database, StoreFront, even the Cloud Connectors are handled). Management via a new web GUI (DaaS.Cloud.com) with REST APIs; Citrix Auto-Scale integrated. Initial OS was Windows Server 2016 RDSH, with Windows 10 multi-user first-day support promised on GA. Four launch regions (West/East US, West Europe, Australia East), 11 global gateway POPs picked nearest to users.

*Bron: blogpost 'What is the Citrix Managed Desktop? 29 bullets to help you on your way' (2019-05-22), basvankaam.com.*

## Verwante notities

- ['Finally' one bill, but the 25-user minimum rules out small shops](citrix-managed-desktop-finally-one-bill.md)
- [Citrix Workspace Cloud (CWC): a managed control plane over the FMA](citrix-workspace-cloud-overview.md)
- [Citrix Workspace Suite and Workspace Services (on Azure) introduced at Synergy 2014](citrix-workspace-suite-services-2014-origins.md)
- [The CWC Cloud Connector](cwc-cloud-connector.md)
- [The key line between Essentials and full Citrix Cloud: VDA placement](essentials-vs-full-citrix-cloud-vda-placement.md)
- [Nerdio Manager for WVD deploys into your own Azure tenant](nerdio-manager-wvd-deploys-in-your-tenant.md)
- [Windows Virtual Desktop: multi-user Windows 10 as DaaS on Azure](wvd-multi-user-windows10-daas-2019.md)
- [WVD is not a near-term threat to Citrix; enterprise features still favor CTX](wvd-not-a-near-term-threat-to-citrix.md)
- [WVD roadmap signals from the 2019 workshop](wvd-roadmap-signals-2019.md)
