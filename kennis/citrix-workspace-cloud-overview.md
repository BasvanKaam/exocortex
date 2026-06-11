---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-09
tags: [cwc, workspace-cloud, fma, hybrid-cloud, daas]
layer: reference
bron: inside-citrix-fma
---

# Citrix Workspace Cloud (CWC): a managed control plane over the FMA

Citrix Workspace Cloud (CWC) relies heavily on the FlexCast Management Architecture; as soon as Citrix introduces a new FMA feature, CWC gets it first, thanks to a phased 'bucket' approach (still under NDA at the book's writing). It is more a managed/management platform than a product, offering services: Apps and Desktops (XenDesktop/XenApp), Mobility Management (XenMobile), Secure Documents (ShareFile), and Life Cycle Management.

Architecture:
- The CWC control centre / control plane sits at the top of the stack; admins use it to manage and configure deployments.
- Resource Locations hold the VDAs, data and applications, owned and controlled by the customer or partner (e.g. a CSP). They can be on-premises, in a datacentre, or in public/private cloud.
- Resource Locations connect to the CWC services platform via Cloud Connectors.

The model: take a normal XenDesktop/XenApp deployment and 'cloudify' the infrastructural/management pieces. Delivery Controllers, SQL database, License Server, Studio, Director and/or StoreFront live up in CWC as part of the Apps and Desktops service; Citrix sets up, configures, manages and maintains them. The customer is left with only VDAs and NetScaler, hosted anywhere they like. Bas calls it the ultimate hybrid cloud model and 'the way forward'. There was also an AppDisks Tech Preview for CWC.

## Verwante notities

- [Citrix Managed Desktop: single-bill DaaS on Citrix-managed Azure](citrix-managed-desktop-model-2019.md)
- [Citrix Service Provider (CSP) program](citrix-service-provider-program.md)
- [Workspace Cloud lacked an on-prem control plane in 2015](citrix-workspace-cloud-control-plane-2015.md)
- [Citrix Workspace Cloud as the hybrid bridge](citrix-workspace-cloud-hybrid-model.md)
- [Citrix Workspace Suite and Workspace Services (on Azure) introduced at Synergy 2014](citrix-workspace-suite-services-2014-origins.md)
- [New FMA features go to the cloud first](cloud-first-feature-delivery-citrix.md)
- [Cloud service models: SaaS, PaaS, IaaS, DaaS](cloud-service-models-saas-paas-iaas-daas.md)
- [CWC authentication and credential handling security](cwc-authentication-credential-handling.md)
- [The CWC Cloud Connector](cwc-cloud-connector.md)
- [CWC as a near-DaaS workaround for Microsoft desktop-OS licensing](cwc-desktop-os-daas-licensing.md)
- [Citrix Lifecycle Management Services and blueprints](cwc-lifecycle-management-services.md)
- [CWC StoreFront hosting options](cwc-storefront-options.md)
- [The key line between Essentials and full Citrix Cloud: VDA placement](essentials-vs-full-citrix-cloud-vda-placement.md)
- [Bas's case for why deep FMA knowledge still matters in the cloud era](why-fma-knowledge-still-matters-relevance.md)
