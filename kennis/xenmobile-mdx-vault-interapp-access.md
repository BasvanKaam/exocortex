---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, xenmobile, mdx, micro-vpn, netscaler, security]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# XenMobile MDX: Vault, Interapp and Access

How it worked in 2013. The AppController is the core: a self-service corporate app store delivering mobile/web/SaaS/HTML5 apps and (with StoreFront) Windows apps and desktops, with per-app SSO and approval workflows. MDX is the security layer, in three parts:
- **MDX Vault**: encrypts and isolates corporate apps and their data in a container, lockable/wipeable by IT, so IT manages the apps not the whole device.
- **MDX Interapp**: MDX-enabled apps only open other MDX-enabled apps (a link in Worx Mail opens Worx Web, not Safari); IT can policy-control cut/paste between protected apps.
- **MDX Access**: policy-based access control checking device type, network, passcode, jailbreak status before an app launches. Introduces the per-app micro VPN into the corporate network (requires NetScaler), avoiding a device-wide VPN.

*Bron: blogpost 'BYOD... Beyond the hype' (2013-08-08), basvankaam.com.*

## Verwante notities

- [Citrix Worx / MDX app containerization model](citrix-worx-mdx-container-model.md)
- [Genuinely enthusiastic about Citrix mobility, MDX as the standout](cloudgateway-fan-not-employee.md)
- [Getting the XenMobile MDM server out of the DMZ was overdue and underdiscussed](mdm-out-of-dmz-relief.md)
- [MDX and the MDX Vault: containerizing corporate mobile apps](mdx-mobile-app-containerization.md)
- [How Citrix made apps Worx-enabled with MDX wrapping](mdx-worx-app-wrapping.md)
- [A technical book should teach the why, not just the clicks](what-a-good-technical-book-should-teach.md)
