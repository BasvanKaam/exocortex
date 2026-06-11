---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [vmware, horizon, blast-extreme, protocol, h264]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# How VMware Blast Extreme worked (Horizon 7 era)

How it worked then (2017, Horizon 7): Blast Extreme was one of three Horizon protocol choices alongside PCoIP and RDP (RDP as fallback). It built on the older HTML5 Blast protocol (around since 2013, first shipped in Horizon View 5.2 Feature Pack 1) and required native clients at 4.x minimum.

Agent-side it ran three components: the VMware Blast service (VMBlastS.exe) managing sessions and proxying TCP; the Blast Worker process (VMBlastW.exe) capturing the screen and handling the session; and, when using UDP, the Blast Proxy process (VMBlastP.exe) brokering UDP connections.

It was based on the H.264 codec (decoded in client hardware where available, else software H.264, else JPG/PNG fallback), used lossy compression by default (lossless optional), and supported Windows, Linux, Android, iOS, Mac, 70+ thin/zero clients, up to four monitors, and the full rich-experience stack (printing, USB redirection, smart cards, MMR, Skype optimisation).

*Bron: blogpost 'In detail -- VMware's Blast Extreme protocol' (2017-02-15), basvankaam.com.*

## Verwante notities

- [Blast Extreme: ports, TCP vs UDP, and GPU offload numbers](blast-extreme-network-and-gpu-behaviour.md)
- [Take: Blast Extreme is an option, not a PCoIP killer](blast-extreme-not-a-pcoip-replacement.md)
- [Citrix HDX display codecs and their confusing alternate names](citrix-hdx-display-codecs-overview.md)
- [Framehawk and the Lightweight Framebuffer Protocol (LFP)](framehawk-lfp-protocol.md)
- [Framehawk's Lightweight Framebuffer Protocol](framehawk-lfp-protocol-2.md)
- [ThinWire compatibility mode: the low-footprint fallback for H.264](thinwire-compatibility-mode.md)
- [VMware Cloud Pod Architecture aggregates pods behind one entitlement layer](vmware-cloud-pod-architecture.md)
