---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, xenmobile, mdx, app-wrapping, ios, android, dated-2014]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# How XenMobile app wrapping, MDX and app signing worked (needed a Mac)

How it worked then (XenMobile, 2014):

- App wrapping used the MDX Toolkit to inject MDX technology around or into an app, turning it into a Worx-enabled app with features like data encryption, password authentication, secure lock and wipe, inter-app policies and micro VPNs (the last needing a NetScaler).
- A hard constraint people forgot: the MDX Toolkit only ran on macOS (OS X 10.7-10.9), so you needed a Mac or iMac. It also required JDK 1.7.
- Before wrapping, mobile apps first had to be signed by Apple or Android. Apple gave you a provisioning profile plus certificate; iOS needed Enterprise (unlimited devices, paid) or Ad Hoc (~100 devices, free) profiles. Citrix recommended the (paid) Enterprise profile. Signing also applied to in-house apps and to the Worx suite (Web, Mail, Notes, Edit, Desktop).

Fully dated to the XenMobile/Worx era, kept as a record of the app-wrapping workflow of the time.

*Bron: blogpost 'XenMobile prerequisits, what do we need and how does it all fit together?' (2014-05-12), basvankaam.com.*

## Verwante notities

- [MDX and the MDX Vault: containerizing corporate mobile apps](mdx-mobile-app-containerization.md)
- [How Citrix made apps Worx-enabled with MDX wrapping](mdx-worx-app-wrapping.md)
- [Adding mobile gestures to Windows apps via the Worx App SDK](mobilizing-windows-apps-worx-sdk.md)
