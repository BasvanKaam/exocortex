---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [hdx, ica, thinwire, framehawk]
layer: rich
bron: inside-citrix-fma
---

# HDX is not a replacement for ICA

A point Bas hammers home: HDX is not a replacement for the ICA protocol. HDX is a set of capabilities/technologies for a high-definition user experience that operate on top of the ICA remoting protocol — an extension, never a substitute.

Related technologies he discusses:
- ThinWire is not new — it has been a core component of the ICA virtual display channel stack for over twenty years. That is why the latest addition was rebranded 'ThinWire Plus' (it has had several names: ThinWire Advanced, Legacy ThinWire, ThinWire compatibility mode). ThinWire is about compressing data, has a small CPU/memory footprint and needs little bandwidth.
- Framehawk targets packet loss and high-latency connections, delivering an acceptable experience under challenging conditions; it generally needs more CPU and bandwidth than ThinWire, though this improved greatly with the 7.8 release.

He cheekily points readers to YouTube Framehawk comparison clips, asking 'Guess who comes out on top?'

## Bron-citaten (NL, verbatim)

> If you go to YouTube and search for Citrix Framehawk you will find multiple comparison clips of Framehawk vs. other technologies. Guess who comes out on top?
