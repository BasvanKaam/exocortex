---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, xendesktop, fma, storefront, netscaler]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# FMA core components: Receiver, StoreFront, NetScaler Gateway

How it worked then (XenDesktop 7.x, 2014): The FlexCast Management Architecture (FMA) underpins both XenApp and XenDesktop since they share the same architecture. Core pieces as Bas lays them out: Receiver runs on the endpoint and talks to NetScaler, StoreFront and the data-center machines over 80/443, using the StoreFront Service API (auth, enumeration, reconnect/disconnect, launch, power control). A StoreFront Web API (Receiver for HTML5) gives browser access with no local Receiver. Within a Site there are two points of authentication: StoreFront (internal) and the NetScaler Gateway (external), and the authentication and enumeration paths differ between internal and external access. StoreFront drives enumeration and the .ICA launch file and is the store users subscribe to. Dated product detail, but the component-interaction mental model is the durable troubleshooting foundation he preaches.

*Bron: blogpost 'The ultimate Citrix XenDesktop 7.x internals cheat sheet!' (2014-11-24), basvankaam.com.*

## Verwante notities

- [The Server VDA is the component everyone overlooked](positie-server-vda-overlooked.md)
