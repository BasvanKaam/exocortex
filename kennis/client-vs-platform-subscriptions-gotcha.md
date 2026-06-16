---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, storefront, app-controller, subscription, dated-2014]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# App subscriptions are stored by the platform, not the client

A non-obvious gotcha Bas surfaced: which client you use (Citrix Receiver vs Worx Home) does not determine your subscription list; the underlying platform does.

- StoreFront stores subscriptions in its (Windows) Extensible Storage Engine database, propagated to other StoreFront servers by the subscription store service. So as long as you go through StoreFront, you get the same app set on every endpoint.
- App Controller stores its own subscriptions independently. Connect to App Controller and you build a separate list.

Consequence: even if you only ever used Receiver to contact both StoreFront and App Controller, you would still end up with two separate subscription lists, because the storage 'platform' differs. Citrix's recommended pattern was Worx Home + App Controller on mobile, Receiver + StoreFront elsewhere, deliberately yielding two lists so mobile and desktop subscriptions could differ. Dated to the XenMobile era but a clean example of 'the client is not the source of truth, the backend is.'

*Bron: blogpost 'How to integrate StoreFront into XenMobile... And than what?!' (2014-04-28), basvankaam.com.*

## Verwante notities

- [Citrix CloudGateway: AppController, StoreFront and Access Gateway](citrix-cloudgateway-architecture.md)
- [How StoreFront and XenMobile App Controller aggregated apps via a trust](storefront-appcontroller-trust-aggregation.md)
- [StoreFront Multi-Site aggregation, mapping and failover](storefront-multisite-aggregation.md)
- [App Controller will eclipse StoreFront as the aggregation point](xenmobile-appcontroller-future-aggregation-point.md)
- [Worx Home as the XenMobile enrollment and communication hub](xenmobile-worx-home-enrollment.md)
