---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, storefront, app-controller, xenmobile, worx-home, dated-2014]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# How StoreFront and XenMobile App Controller aggregated apps via a trust

How it worked then (2014, XenMobile / App Controller 2.10):

- App Controller delivered Mobile, Web and SaaS apps (and ShareFile data). Apps were signed, then wrapped with MDX binaries, then uploaded and assigned to users, appearing in the App Controller App Store (a.k.a. the Receiver/Worx Home App Store).
- StoreFront's Store Service handled enumeration/aggregation and could query different content providers: the XML broker service for XenApp/XenDesktop resources, and App Controller for ShareFile, web, SaaS and mobile apps.
- To make StoreFront aggregate App Controller apps you configured a trust, initiated from App Controller (Settings > 'Allow StoreFront to aggregate App Controller apps', enter StoreFront FQDN), then added App Controller as a Delivery Controller in StoreFront. It was a two-step, both-sides handshake.
- To launch Windows apps/desktops from Worx Home, you also configured 'Windows App Settings' in App Controller with a Relative Path that enabled PNAgent functionality on StoreFront. Even then, Citrix Receiver still had to be installed to handle the actual launch, because Worx Home lacked the XML processing capability by design.

Dated UI and product names, but the underlying pattern (an aggregation point trusting multiple content providers) is the lineage of later Citrix Workspace.

*Bron: blogpost 'How to integrate StoreFront into XenMobile... And than what?!' (2014-04-28), basvankaam.com.*

## Verwante notities

- [Citrix CloudGateway: AppController, StoreFront and Access Gateway](citrix-cloudgateway-architecture.md)
- [App subscriptions are stored by the platform, not the client](client-vs-platform-subscriptions-gotcha.md)
- [MDX and the MDX Vault: containerizing corporate mobile apps](mdx-mobile-app-containerization.md)
- [ShareFile is miles ahead of the competition (2017 take)](sharefile-miles-ahead-of-competition.md)
- [StoreFront 2.0 replaces Web Interface (key features)](storefront-2-replaces-web-interface.md)
- [StoreFront multi-Site: aggregation, user mapping and recovery sites](storefront-multi-site-aggregation-and-user-mapping.md)
- [StoreFront over Web Interface, and StoreFront design notes](storefront-over-web-interface.md)
- [StoreFront over Web Interface is a good thing (April 2013)](storefront-over-web-interface-call.md)
- [App Controller will eclipse StoreFront as the aggregation point](xenmobile-appcontroller-future-aggregation-point.md)
- [Worx Home as the XenMobile enrollment and communication hub](xenmobile-worx-home-enrollment.md)
