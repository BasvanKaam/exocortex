---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [framehawk, hdx, packet-loss, latency, mobile]
layer: reference
bron: inside-citrix-fma
---

# Framehawk: ICA over lossy, high-latency networks

Framehawk was first introduced with Feature Pack 2 for XenDesktop/XenApp 7.6 with a new Receiver (4.3). It is aimed at mobile workers on Wi-Fi/4G where packet loss and high latency are problems. Bas notes Framehawk still delivered an acceptable experience at latencies up to 500 ms and 35% packet loss, which he calls impressive.

Framehawk generally consumes more bandwidth and CPU than ThinWire compatibility mode. With the 7.8 releases it improved significantly: ~40% reduction in memory footprint, up to 20% CPU efficiency, and up to 50% bandwidth efficiency when scrolling via touch input. It became compatible with the latest NetScaler Gateway (including Unified Gateway as of 11.0-F) and Citrix Receiver for Windows and iOS. Choosing between Framehawk and ThinWire depends on the use case.
