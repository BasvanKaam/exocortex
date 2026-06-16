---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-09
tags: [cwc, storefront, security, 2fa]
layer: reference
bron: inside-citrix-fma
---

# CWC StoreFront hosting options

With CWC you choose where to host StoreFront, which affects custom domain names and URLs:
- Cloud-hosted StoreFront: the Apps and Desktops service hosts a StoreFront site per customer. Zero deployment effort, kept evergreen by Citrix. Recommended for all new customers, previews, and PoCs.
- On-premises StoreFront: customers can use an existing StoreFront to aggregate cloud apps/desktops. Offers greater security including two-factor authentication, prevents users entering passwords into the cloud service, and allows custom domain names/URLs. Recommended for existing XenApp/XenDesktop customers who already have StoreFront.
- A combination of on-premises and cloud-hosted StoreFront.

## Verwante notities

- [Citrix Workspace Cloud credential and authentication handling](citrix-workspace-cloud-credential-handling.md)
- [Citrix Workspace Cloud (CWC): a managed control plane over the FMA](citrix-workspace-cloud-overview.md)
- [CWC authentication and credential handling security](cwc-authentication-credential-handling.md)
- [The CWC Cloud Connector](cwc-cloud-connector.md)
- [Citrix Lifecycle Management Services and blueprints](cwc-lifecycle-management-services.md)
- [External user authentication through NetScaler](external-authentication-through-netscaler.md)
- [Securing StoreFront connections with SSL and NetScaler](securing-storefront-connections-with-ssl.md)
- [StoreFront high availability and Delivery Controller load balancing](storefront-ha-and-load-balancing.md)
