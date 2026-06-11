---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, storefront, web-interface, receiver, follow-me-apps]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# StoreFront 2.0 replaces Web Interface (key features)

How it worked in the XD7 era. StoreFront 2.0 replaced Web Interface and became part of the default XD7 install, manageable from Studio. Notable features:
- Clientless (HTML5) Receiver: full HDX content access in a browser when Receiver can't/won't be installed, traffic routed through StoreFront.
- NetScaler HDX SmartAccess: endpoint analysis (anti-virus, client firewall, drive encryption checks) before passing a connection through.
- Unified app stores with self-service subscription.
- Follow-me apps / device roaming: tracks subscriptions and maintains persistent connections so users can switch devices and continue where they left off ('StoreFront is the intelligence behind Receiver').
- No more external SQL DB dependency: subscriptions and config stored internally.
- Pre-launch.

*Bron: blogpost 'XenDesktop 7 editions explained' (2013-06-27), basvankaam.com.*

## Verwante notities

- [Citrix dropped the Chromebook Receiver for HTML5](citrix-chromebook-receiver-to-html5.md)
- [Citrix CloudGateway: AppController, StoreFront and Access Gateway](citrix-cloudgateway-architecture.md)
- [Intelligent Configuration Validation and built-in Profile Management](excalibur-built-in-config-validation.md)
- [Time to finally let go of Web Interface and consolidate Receiver](finally-let-go-of-web-interface.md)
- [IMA-to-FMA terminology: Farm to Site, Data Collector to Delivery Controller](ima-to-fma-terminology-map.md)
- [One is none: always deploy two StoreFronts and two Delivery Controllers](one-is-none-storefront-dc-redundancy.md)
- [Three ways to reach resources via Receiver, including HTML5 clientless access](receiver-three-ways-and-html5-clientless.md)
- [Enabling the Unified Receiver Experience in StoreFront 3.0](storefront-3-unified-experience-enable-order.md)
- [How StoreFront and XenMobile App Controller aggregated apps via a trust](storefront-appcontroller-trust-aggregation.md)
- [StoreFront over Web Interface, and StoreFront design notes](storefront-over-web-interface.md)
- [StoreFront over Web Interface is a good thing (April 2013)](storefront-over-web-interface-call.md)
- [StoreFront vs Web Interface user authentication](storefront-vs-web-interface-authentication.md)
- [StoreFront authenticates locally, Web Interface delegates via XML](storefront-vs-webinterface-auth-flow.md)
- [Keep Web Interface when migrating, choose StoreFront when greenfield (April 2013)](web-interface-vs-storefront-migration-call.md)
