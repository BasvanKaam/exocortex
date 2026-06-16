---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, mdx, mam, micro-vpn, byod, mobile]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# MDX and the MDX Vault: containerizing corporate mobile apps

How it worked then (2013). MDX was Citrix's mobile app management layer in CloudGateway, targeted at iOS and Android (HTML5 apps could use it too). The core idea is containerization: corporate web, SaaS, HTML5 and mobile apps plus their data live in the **MDX Vault**, separated from personal apps on the same device, so IT manages only the business apps, not the whole device. Vault apps can be encrypted, remotely locked and wiped.

Three sub-capabilities:
- **MDX Interapp** — MDX-enabled apps only open other MDX-enabled apps (a link in @WorkMail opens @WorkWeb, not Safari); cut/paste can be policy-controlled between containerized apps.
- **MDX Access** — policy-based access control checking device type, network, passcode, jailbreak status, etc. Introduced the **Micro VPN**: an application-specific VPN tunnel into the corporate network, avoiding a device-wide VPN so only the single app reaches internal resources.

Apps were 'wrapped' before publishing via an integrated toolkit that injected the management/policy code. iOS apps still required Apple provisioning profiles and certificates (Enterprise = unlimited devices, Ad Hoc = ~100 devices) before legal distribution; the wrapping/signing itself was free of charge. The native @WorkMail and @WorkWeb apps were built on these MDX features.

This is the conceptual ancestor of later MAM/per-app-VPN approaches still used today.

*Bron: blogpost 'The Citrix CloudGateway' (2013-02-03), basvankaam.com.*

## Verwante notities

- [Byte Squared brought native iOS Office editing into the Citrix Worx stack](bytesquared-office-editing-ios-2013.md)
- [Citrix CloudGateway: AppController, StoreFront and Access Gateway](citrix-cloudgateway-architecture.md)
- [Citrix Worx / MDX app containerization model](citrix-worx-mdx-container-model.md)
- [Genuinely enthusiastic about Citrix mobility, MDX as the standout](cloudgateway-fan-not-employee.md)
- [Two ways to do Dual Persona: app wrapping vs on-device hypervisor](dual-persona-containerization-vs-hypervisor.md)
- [Mobile management acronyms: MDM, MAM, MIM, EMM](mdm-mam-mim-emm-glossary.md)
- [How Citrix made apps Worx-enabled with MDX wrapping](mdx-worx-app-wrapping.md)
- [Adding mobile gestures to Windows apps via the Worx App SDK](mobilizing-windows-apps-worx-sdk.md)
- [How StoreFront and XenMobile App Controller aggregated apps via a trust](storefront-appcontroller-trust-aggregation.md)
- [How XenMobile app wrapping, MDX and app signing worked (needed a Mac)](xenmobile-mdx-app-signing-2014.md)
- [XenMobile MDX: Vault, Interapp and Access](xenmobile-mdx-vault-interapp-access.md)
- [XenMobile PIN + certificate as two-factor auth](xenmobile-pin-certificate-2fa.md)
