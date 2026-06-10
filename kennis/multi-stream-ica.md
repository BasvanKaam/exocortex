---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [multi-stream-ica, qos, streams, session-reliability, tcp-ports]
layer: reference
bron: inside-citrix-fma
---

# Multi-Stream ICA: true network-level QoS via separate TCP/IP ports

Virtual-channel priorities only offer limited control. Multi-Stream (Multi-Port) ICA enables true network-based QoS by assigning separate TCP/IP ports to each priority group (a.k.a. stream). Without it you can only accelerate ICA as a whole on port 1494 or 2598. With it you can give priority-0 channels one port, priority-1 channels another, etc., up to four Multi-Stream ports.

The registry key (when enabled): `HKLM\SYSTEM\CurrentControlSet\Control\Terminal Server\Wds\icawd\MultiStreamIca`, with two subkeys: Stream and VirtualChannels.

- **Stream** key configures stream priorities and primary/secondary assignment, format `Stream#,Streamtype` (e.g. `0,S` = priority-0 channels secondary; `1,P` = priority-1 primary). Only one primary; default config `0,S;1,P;2,S;3,S`.
- **VirtualChannel** key binds VCs to streams, format `VirtualChannelName,Stream#` (e.g. `CTXCAM,1`).

When not using a CloudBridge appliance, Session Reliability must be enabled for Multi-Stream ICA to work. After configuring streams and pairs, set up a multi-port Citrix policy assigning TCP/IP ports to the primary (one) and secondary (three) streams, then apply network-level QoS policies per port (on grouped channels rather than single channels).

## Verwante notities

- [Bas's checklist to speed up and clean up Citrix printing](bas-citrix-printing-optimization-checklist.md)
- [Bas: forcing the client printing pathway (and its exception)](bas-forcing-client-printing-pathway.md)
- [Framehawk: ICA over lossy, high-latency networks](framehawk.md)
- [ICA ports, virtual channels and priorities](ica-ports-and-virtual-channels.md)
- [What the ICA protocol does and its default ports](ica-protocol-fundamentals.md)
- [ICA virtual channel priorities (0-3) and how to change them](ica-virtual-channel-priorities.md)
- [ICA virtual channels: 32 total, 17 reserved by Citrix](ica-virtual-channels.md)
- [Session Reliability, Auto Client Reconnect and ICA Keep-Alive](session-reliability-and-auto-reconnect.md)
