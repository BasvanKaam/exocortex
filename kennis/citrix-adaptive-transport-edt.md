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
