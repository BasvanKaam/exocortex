---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [ica, virtual-channels, ports, session-reliability, cgp]
layer: reference
bron: inside-citrix-fma
---

# ICA ports, virtual channels and priorities

ICA uses TCP port 1494 by default. When Session Reliability (the Common Gateway Protocol, CGP) is enabled, ICA traffic is encapsulated/tunnelled through TCP port 2598 — so network traces will show 2598 instead of 1494.

ICA has 32 virtual channels in total, 17 of which Citrix reserves; third parties and customers can build their own using the remaining ones (dynamic virtual channels / DVCs). Client capabilities are negotiated at session launch (the handshake). Each virtual channel has a default priority from 0 to 3, with 0 the highest (more priority = more bandwidth). Priorities can be changed via the registry, but raising one channel takes bandwidth from another. Multi-Stream ICA assigns separate TCP/IP ports to groups of priorities (streams) to establish true QoS. Citrix recommends, as a security best practice, disabling any virtual channels not in use.
