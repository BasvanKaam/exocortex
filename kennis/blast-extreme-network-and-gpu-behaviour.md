---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [vmware, blast-extreme, networking, nvidia-grid, udp]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Blast Extreme: ports, TCP vs UDP, and GPU offload numbers

How it worked then (2017): Blast Extreme used TCP by default (UDP had to be configured explicitly) over external ports 443 (HTTPS) and 8443 (TCP/UDP). Remote-experience traffic flowed through the VMware Virtual Channel on port 22443; MMR and USB redirection used side channels on ports 9427 and 32111. VMware recommended keeping MMR and Client Drive Redirection on the side channels rather than routing them through the virtual channel, because doing so cost performance.

On lossy networks, H.264 over TCP tolerated up to ~20% packet loss and over UDP up to ~25%. With NVIDIA GRID H.264 hardware encoding (GRID K1, K2, M6, M10, M60), VMware claimed up to 50 ms lower latency, over 80% bandwidth reduction on TCP and up to 19% on UDP versus PCoIP, plus 4K support. AMD multi-user GPU (S7150, S715x2, S7100X) could split one GPU among 2 to 15 users. Hardware H.264 decode on the client also saved battery.

*Bron: blogpost 'In detail -- VMware's Blast Extreme protocol' (2017-02-15), basvankaam.com.*

## Verwante notities

- [Take: Blast Extreme is an option, not a PCoIP killer](blast-extreme-not-a-pcoip-replacement.md)
- [How VMware Blast Extreme worked (Horizon 7 era)](blast-extreme-protocol-internals.md)
- [Citrix HDX display codecs and their confusing alternate names](citrix-hdx-display-codecs-overview.md)
- [EDT and HDX.next milestones announced at Summit 2017](citrix-summit-2017-edt-hdx-gains.md)
- [GPUs in VDI: a tool in the toolbox, not a default](gpu-in-vdi-tool-in-the-toolbox.md)
- [Intel entering vGPU turns the GPU space into a three-way race](intel-enters-vgpu-three-way-race.md)
- [ThinWire compatibility mode: the low-footprint fallback for H.264](thinwire-compatibility-mode.md)
