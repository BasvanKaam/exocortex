---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, hdx, thinwire, framehawk, h264, dcr, display, graphics-mode]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Citrix HDX display codecs and their confusing alternate names

How it worked then (2016): Citrix display modes, with the alternate names they show under HDX Monitor: DCR (Desktop Composition Redirection) = Direct 3D in HDX Monitor; H.264 / 264 Compatibility Mode = Thinwire Advanced in HDX Monitor; Legacy Graphics Mode = Thinwire in HDX Monitor; and Framehawk. Which mode is used is determined by the policies set and their hierarchy. A known source of confusion: in Studio all display policies are mixed together, some policies (e.g. adaptive display) apply to multiple modes (legacy AND Thinwire compatibility), documentation wasn't always updated with the latest names, and HDX Thinwire (introduced with XenDesktop Feature Pack 3) recently replaced Compatibility Mode. Finding which codec is actually in use, and with which settings, was hard, typically via HDX Monitor (local or via Director) or WMI queries from a command prompt.

*Bron: blogpost 'Presenting... The Remote Display Analyzer!' (2016-02-23), basvankaam.com.*

## Verwante notities

- [Blast Extreme: ports, TCP vs UDP, and GPU offload numbers](blast-extreme-network-and-gpu-behaviour.md)
- [How VMware Blast Extreme worked (Horizon 7 era)](blast-extreme-protocol-internals.md)
- [Citrix Adaptive Transport (Enlightened Data Transport / EDT)](citrix-adaptive-transport-edt.md)
- [Citrix HDX: an extension to ICA, not a replacement](citrix-hdx-extends-ica.md)
- [EDT and HDX.next milestones announced at Summit 2017](citrix-summit-2017-edt-hdx-gains.md)
- [Framehawk and the Lightweight Framebuffer Protocol (LFP)](framehawk-lfp-protocol.md)
- [HDX Browser Content Redirection renders client-side via CEF](hdx-browser-content-redirection-cef.md)
- [HDX extends ICA, it does not replace it](hdx-extends-ica-not-replaces.md)
- [HDX Monitor: HDX diagnostics tool](hdx-monitor-tool.md)
- [ICA connection renamed HDX connection (terminology shift, 2013)](ica-connection-becomes-hdx-connection.md)
- [Delivering Lync in a XenApp hosted shared desktop: generic vs optimized HDX](lync-xenapp-delivery-options.md)
- [RDA is an industry first that out-shipped Citrix itself](positie-rda-industry-first.md)
- [Remote Display Analyzer: detect and live-switch HDX codecs](remote-display-analyzer-tool.md)
- [ThinWire compatibility mode: the low-footprint fallback for H.264](thinwire-compatibility-mode.md)
