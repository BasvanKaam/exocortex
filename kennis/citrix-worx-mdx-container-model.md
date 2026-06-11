---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, xenmobile, worx, mdx, containerization, micro-vpn]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Citrix Worx / MDX app containerization model

How it worked in XenMobile 8.5 (2013). The approach to MAM: apps are made 'Worx-enabled' (MDX-enabled) and kept in a secure container so they can only interact with other Worx-enabled apps (MDX Interapp communication), keeping corporate apps walled off from personal ones on the same device. MDX adds data encryption, password authentication, secure lock/wipe, inter-app policies, and per-app micro VPNs.

Any app could be Worx-enabled via the Worx App SDK with 'a single line of code', or by wrapping post-development without code changes. Citrix ran a 'Citrix Ready Worx Verified' program; over 65 ISVs (Adobe, IBM, Cisco) had committed to shipping Worx-enabled apps, downloadable from a forthcoming Worx App Gallery.

Worx Home was the central client app (replacing Receiver's role for mobile/SaaS/web apps), used to enroll, access the unified app store, and reach one-click live support (GoToAssist). The June 2013 release did not yet support Windows apps/desktops, for those you still needed Receiver alongside it.

*Bron: blogpost 'XenMobile what's new?!' (2013-07-08), basvankaam.com.*

## Verwante notities

- [BYOD has graduated from hype to something you can't ignore](byod-from-hype-to-unavoidable.md)
- [2013 mobile management vendor landscape](byod-vendor-landscape-2013.md)
- [Citrix's constant rebranding confuses customers](citrix-rebranding-confuses-people.md)
- [A self-declared Citrix hugger who still tells you to shop around](citrix-self-aware-bias-but-look-at-vendors.md)
- [Mobile management acronyms: MDM, MAM, MIM, EMM](mdm-mam-mim-emm-glossary.md)
- [MDX and the MDX Vault: containerizing corporate mobile apps](mdx-mobile-app-containerization.md)
- [How Citrix made apps Worx-enabled with MDX wrapping](mdx-worx-app-wrapping.md)
- [Adding mobile gestures to Windows apps via the Worx App SDK](mobilizing-windows-apps-worx-sdk.md)
- [XenMobile a leading EMM platform on broad device support (2014)](xenmobile-leading-emm-2014.md)
- [XenMobile MDX: Vault, Interapp and Access](xenmobile-mdx-vault-interapp-access.md)
- [Worx Home as the XenMobile enrollment and communication hub](xenmobile-worx-home-enrollment.md)
