---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, cloud-gateway, storefront, appcontroller, gateway, byod]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Citrix CloudGateway: AppController, StoreFront and Access Gateway

How it worked then (2013). CloudGateway was Citrix's suite for building an on-premises private cloud that delivered Windows, web, SaaS, mobile and HTML5 apps plus ShareFile data through a single self-service store, accessible securely from anywhere.

Three key components:
- **AppController** — a virtual appliance (on XenServer, also VMware ESXi) that securely delivers web, SaaS, mobile and HTML5 apps plus integrated ShareFile data. Handles per-application SSO via configurable SSO connectors, and automated provisioning/deprovisioning driven by Active Directory group membership (an AD security group per app).
- **StoreFront** — the next-generation Web Interface, a modular redesign reusing most Web Interface code. Creates the centralized enterprise app store, handles authentication/SSO, application enumeration (querying the XML service for XenApp/XenDesktop and AppController for everything else), and launch. Sub-elements: Receiver for Web, Authentication, Store, Gateways, Beacons.
- **Access Gateway** — single point for secure remote access and policy-based access control, including HDX SmartAccess endpoint analysis.

Editions: Express (free for XenApp/XenDesktop customers, Windows apps/desktops only) and Enterprise (adds mobile, web and ShareFile delivery to any device).

Internal-vs-external detection used two mechanisms: native Receivers use **beacons** (ping an internal-only address = internal; reachable only externally, e.g. Yahoo.com = external), while Receiver for Web uses a **remote flag** in the HTTP header plus a 'remote flag call-back' that the Store service confirms against the Access Gateway.

*Bron: blogpost 'The Citrix CloudGateway' (2013-02-03), basvankaam.com.*

## Verwante notities

- [Beacon-based Receiver connection routing](beacon-based-receiver-connection-routing.md)
- [App subscriptions are stored by the platform, not the client](client-vs-platform-subscriptions-gotcha.md)
- [Genuinely enthusiastic about Citrix mobility, MDX as the standout](cloudgateway-fan-not-employee.md)
- [MDX and the MDX Vault: containerizing corporate mobile apps](mdx-mobile-app-containerization.md)
- [ShareFile is miles ahead of the competition (2017 take)](sharefile-miles-ahead-of-competition.md)
- [StoreFront 2.0 replaces Web Interface (key features)](storefront-2-replaces-web-interface.md)
- [How StoreFront and XenMobile App Controller aggregated apps via a trust](storefront-appcontroller-trust-aggregation.md)
- [App Controller will eclipse StoreFront as the aggregation point](xenmobile-appcontroller-future-aggregation-point.md)
