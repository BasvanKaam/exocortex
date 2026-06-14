---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, hdx, ica, protocol, concept]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# HDX extends ICA, it does not replace it

How it worked then (XenApp/XenDesktop 7.x era): HDX is not a replacement for the ICA protocol. HDX is a set of capabilities/technologies delivering a high-definition user experience, built on top of the ICA remoting protocol. The ICA protocol itself originated with Citrix Multiuser around 1990/1991, making it over 25 years old at the time of writing. By default ICA uses TCP 1494; with Session Reliability (the Common Gateway Protocol, CGP) enabled, ICA traffic is encapsulated over TCP 2598, which is what shows up in network traces. ThinWire is a core component of the ICA virtual display channel stack and has been there for twenty-plus years, despite being marketed as new (rebranded ThinWire Plus). Of the 32 virtual channels, Citrix reserves 17; the rest are open for third-party/customer dynamic virtual channels (DVCs).

*Bron: blogpost '100+ Citrix XenApp & XenDesktop FMA facts listed' (2017-04-11), basvankaam.com.*

## Verwante notities

- [Take: Blast Extreme is an option, not a PCoIP killer](blast-extreme-not-a-pcoip-replacement.md)
- [Citrix HDX display codecs and their confusing alternate names](citrix-hdx-display-codecs-overview.md)
- [Citrix HDX: an extension to ICA, not a replacement](citrix-hdx-extends-ica.md)
- [Framehawk and the Lightweight Framebuffer Protocol (LFP)](framehawk-lfp-protocol.md)
- [HDX Browser Content Redirection renders client-side via CEF](hdx-browser-content-redirection-cef.md)
- [ICA connection renamed HDX connection (terminology shift, 2013)](ica-connection-becomes-hdx-connection.md)
- [Delivering Lync in a XenApp hosted shared desktop: generic vs optimized HDX](lync-xenapp-delivery-options.md)
- [ThinWire compatibility mode: the low-footprint fallback for H.264](thinwire-compatibility-mode.md)
