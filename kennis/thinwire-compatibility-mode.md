---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [thinwire, hdx, h264, compatibility-mode, user-density]
layer: reference
bron: inside-citrix-fma
---

# ThinWire compatibility mode: the low-footprint fallback for H.264

ThinWire has been part of ICA almost from the start (WinFrame 1995, ICA 3.0). ThinWire compatibility mode (also called project snowball, enhanced ThinWire, ThinWire Plus, etc.) was released with Feature Pack 3 for XenDesktop/XenApp 7.6 and improved again in 7.8 with enhanced lossless visual quality, sharpening fuzzy images faster than 7.7.

It is a fallback for the default 'video codec for compression', which uses H.264 and delivers high-quality graphics/video for most users by default. The H.264 method consumes more resources to encode/decode, needing a high-power client processor and impacting server-side user density.

If the default method can't kick in (insufficient client CPU, or an older unsupported Receiver), ThinWire compatibility mode is used automatically. It uses low-cost algorithms compatible with almost every OS, with a very efficient CPU and bandwidth footprint. Bas suggests that even when the default mode works you might consider switching to compatibility mode anyway, to enhance user density and save resources and bandwidth. Studio ships 6 HDX policy templates.

## Verwante notities

- [Blast Extreme: ports, TCP vs UDP, and GPU offload numbers](blast-extreme-network-and-gpu-behaviour.md)
- [How VMware Blast Extreme worked (Horizon 7 era)](blast-extreme-protocol-internals.md)
- [Citrix Adaptive Transport (Enlightened Data Transport / EDT)](citrix-adaptive-transport-edt.md)
- [Citrix HDX display codecs and their confusing alternate names](citrix-hdx-display-codecs-overview.md)
- [Citrix HDX: an extension to ICA, not a replacement](citrix-hdx-extends-ica.md)
- [Framehawk: ICA over lossy, high-latency networks](framehawk.md)
- [Framehawk and the Lightweight Framebuffer Protocol (LFP)](framehawk-lfp-protocol.md)
- [HDX Browser Content Redirection renders client-side via CEF](hdx-browser-content-redirection-cef.md)
- [HDX extends ICA, it does not replace it](hdx-extends-ica-not-replaces.md)
- [HDX is not a replacement for ICA](hdx-not-a-replacement-for-ica.md)
- [What the ICA protocol does and its default ports](ica-protocol-fundamentals.md)
- [Receiver communications, ICA handshake and virtual channels](receiver-ica-handshake-and-virtual-channels.md)
- [Remote Display Analyzer: a community HDX codec tool](remote-display-analyzer.md)
