---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, xenmobile, mdm, cloudgateway, mobility]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# XenMobile editions: MDM vs Mobile Solutions Bundle (how it worked in 2013)

In the first XenMobile release after Citrix acquired Zenprise, there were two editions. XenMobile MDM focused on hardware device management (enrollment, policies, lock/wipe) across iPhone, iPad, Android, BlackBerry, Symbian and Windows 8. It shipped with the Secure Mobile Gateway (SMG), SharePoint DLP, the Mobile Service Provider (ZSM) and a Remote Support toolset. The Mobile Solutions Bundle added the CloudGateway (AppController) on top, giving web/SaaS/HTML5 and ShareFile-based app and data delivery.

Key 2013 framing: MDM primarily manages the device; the application layer is handled by AppController. To also publish Windows apps, hosted shared desktops or VDIs through XenApp/XenDesktop you additionally needed StoreFront. Many of the newer CloudGateway security features were only compatible with iOS and Android at the time.

*Bron: blogpost 'XenMobile product overview… and It's nice!' (2013-03-12), basvankaam.com.*

## Verwante notities

- [MDM enrollment binds both the device and the user (durable concept)](mdm-enrollment-device-then-user.md)
