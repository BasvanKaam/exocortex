---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [xenmobile, mdx, worx, mam, mobility, citrix]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# How Citrix made apps Worx-enabled with MDX wrapping

How it worked then (XenMobile 8.x): an app published via AppController was a "Worx-enabled" app. It lived in a secure vault, isolated from personal apps and data, could only talk to other vault apps when allowed, and used micro VPNs (with NetScaler) for a secure tunnel to the datacenter app.

Apps became Worx-enabled by applying MDX (Mobile Device Experience), which Citrix called "wrapping": adding an MDX layer that delivered the shared characteristics, named MDX App Vault, MDX Access and MDX InterApp. The Worx App SDK did the wrapping; the MDX library could be embedded with a single line of code, or apps could be wrapped post-development with no code change. MDX added data encryption, password auth, secure lock and wipe, inter-app policies and micro VPNs, all configurable per app.

Bas's note: Citrix mixing up terms is what confuses people; the one thing to remember is that a Worx app is simply an app wrapped with MDX.

*Bron: blogpost 'Citrix XenMobile (8.6) revisited' (2013-11-02), basvankaam.com.*

## Verwante notities

- [BYOD has graduated from hype to something you can't ignore](byod-from-hype-to-unavoidable.md)
- [2013 mobile management vendor landscape](byod-vendor-landscape-2013.md)
- [Byte Squared brought native iOS Office editing into the Citrix Worx stack](bytesquared-office-editing-ios-2013.md)
- [Citrix Worx / MDX app containerization model](citrix-worx-mdx-container-model.md)
- [Genuinely enthusiastic about Citrix mobility, MDX as the standout](cloudgateway-fan-not-employee.md)
- [Mobile management acronyms: MDM, MAM, MIM, EMM](mdm-mam-mim-emm-glossary.md)
- [MDX and the MDX Vault: containerizing corporate mobile apps](mdx-mobile-app-containerization.md)
- [Adding mobile gestures to Windows apps via the Worx App SDK](mobilizing-windows-apps-worx-sdk.md)
- [A technical book should teach the why, not just the clicks](what-a-good-technical-book-should-teach.md)
- [How XenMobile app wrapping, MDX and app signing worked (needed a Mac)](xenmobile-mdx-app-signing-2014.md)
- [XenMobile MDX: Vault, Interapp and Access](xenmobile-mdx-vault-interapp-access.md)
- [Worx Home as the XenMobile enrollment and communication hub](xenmobile-worx-home-enrollment.md)
