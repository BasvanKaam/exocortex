---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [edt, adaptive-transport, udp, ica, hdx]
layer: reference
bron: inside-citrix-fma
---

# Citrix Adaptive Transport (Enlightened Data Transport / EDT)

As of XenDesktop 7.13, Adaptive Transport (also known as Enlightened Data Transport, or EDT) is available for production. EDT also refers to the policy needed to enable Adaptive Transport. This new transport layer above UDP improves data throughput for all ICA virtual channels, including printing. It prefers the Citrix EDT protocol over TCP whenever possible, falling back to TCP when UDP is unavailable.

## Verwante notities

- [Citrix HDX display codecs and their confusing alternate names](citrix-hdx-display-codecs-overview.md)
- [EDT and HDX.next milestones announced at Summit 2017](citrix-summit-2017-edt-hdx-gains.md)
- [Framehawk: ICA over lossy, high-latency networks](framehawk.md)
- [Framehawk and the Lightweight Framebuffer Protocol (LFP)](framehawk-lfp-protocol.md)
- [HDX is not a replacement for ICA](hdx-not-a-replacement-for-ica.md)
- [Session Reliability, Auto Client Reconnect and ICA Keep-Alive](session-reliability-and-auto-reconnect.md)
- [ThinWire compatibility mode: the low-footprint fallback for H.264](thinwire-compatibility-mode.md)
