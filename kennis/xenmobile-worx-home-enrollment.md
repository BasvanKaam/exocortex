---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, xenmobile, worx, mdm, enrollment]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Worx Home as the XenMobile enrollment and communication hub

How it worked then (2014): before a device could be managed or have apps pushed, it had to enroll and get known by the MDM server. Enrollment used a single free app, Worx Home, downloaded from the app stores, after which a simple wizard completed registration. From then on all communication between the device and the various backend systems flowed through the Worx Home app. In a BYOD scenario IT managed only the business side; private apps and data stayed isolated, with the two sides unable to communicate unless the user allowed it.

*Bron: blogpost '16 random reasons to (at least) consider Citrix XenMobile' (2014-02-12), basvankaam.com.*

## Verwante notities

- [Citrix Worx / MDX app containerization model](citrix-worx-mdx-container-model.md)
- [App subscriptions are stored by the platform, not the client](client-vs-platform-subscriptions-gotcha.md)
- [MDM enrollment binds both the device and the user (durable concept)](mdm-enrollment-device-then-user.md)
- [How Citrix made apps Worx-enabled with MDX wrapping](mdx-worx-app-wrapping.md)
- [Adding mobile gestures to Windows apps via the Worx App SDK](mobilizing-windows-apps-worx-sdk.md)
- [How StoreFront and XenMobile App Controller aggregated apps via a trust](storefront-appcontroller-trust-aggregation.md)
- [XenMobile PIN + certificate as two-factor auth](xenmobile-pin-certificate-2fa.md)
