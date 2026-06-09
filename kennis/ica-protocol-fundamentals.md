---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [ica, remoting-protocol, port-1494, cgp, thinwire]
layer: reference
bron: inside-citrix-fma
---

# What the ICA protocol does and its default ports

At a high level, the ICA protocol transports keystrokes, mouse clicks and screen updates (over standard protocols like TCP/IP, IPX, NetBEUI, SPX) from server to client in a controlled, secure manner. It is optimised for high-latency WANs and offers various Quality of Service levels. Such protocols are called remoting protocols.

By default ICA uses TCP port 1494. If Session Reliability (a.k.a. the Common Gateway Protocol, CGP) is enabled, ICA traffic is encapsulated through TCP port 2598; network traces then show 2598 instead of 1494.

When WinFrame launched (1995) it introduced ICA 3.0 including ThinWire 1.0; ICA functionality was then limited to ThinWire (screen updates), printing, client drive mapping and audio. Earlier ICA 1.0 and 2.0 both shipped in 1992 with the Citrix Multiuser launch.
