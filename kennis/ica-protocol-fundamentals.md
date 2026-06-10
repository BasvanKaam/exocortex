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

## Verwante notities

- [Citrix HDX: an extension to ICA, not a replacement](citrix-hdx-extends-ica.md)
- [HDX is not a replacement for ICA](hdx-not-a-replacement-for-ica.md)
- [The origin of Citrix and the ICA protocol](history-of-citrix-and-ica.md)
- [ICA ports, virtual channels and priorities](ica-ports-and-virtual-channels.md)
- [ICA protocol origin and the birth of Microsoft RDP](ica-protocol-origin-and-rdp.md)
- [ICA virtual channels: 32 total, 17 reserved by Citrix](ica-virtual-channels.md)
- [Multi-Stream ICA: true network-level QoS via separate TCP/IP ports](multi-stream-ica.md)
- [Receiver communications, ICA handshake and virtual channels](receiver-ica-handshake-and-virtual-channels.md)
- [Session Reliability, Auto Client Reconnect and ICA Keep-Alive](session-reliability-and-auto-reconnect.md)
- [ThinWire compatibility mode: the low-footprint fallback for H.264](thinwire-compatibility-mode.md)
