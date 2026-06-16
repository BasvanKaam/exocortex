---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [vda, install-options, supported-os, remote-pc, pvd]
layer: reference
bron: inside-citrix-fma
---

# VDA install options and supported operating systems

Supported VDA operating systems:
- Server VDA: Windows Server 2008 R2, Windows Server 2012 and R2, Windows Server 2016.
- Desktop VDA: Windows 7 SP1 (Professional, Enterprise, Ultimate), Windows 8 and 8.1 (Professional, Enterprise), and as of XenDesktop 7.6 Feature Pack 3, Windows 10 Enterprise.
- Linux (desktop and server): SUSE, Red Hat, CentOS, Ubuntu.

The Server VDA is far more lightweight than the old XenApp full install, even lighter than XenApp 6.5 'Session only mode': it consists only of components needed to host sessions and does not share Delivery Controller components.

Manual install options (defaults shown):
- Optimize performance (on by default): VM optimization for VDAs on a hypervisor, disables offline files, disables background defragmentation, reduces event log size. Do NOT enable for Remote PC Access.
- Windows Remote Assistance (on by default): used with Director user-shadowing; Windows auto-opens TCP port 3389.
- Real-Time Audio Transport for audio (on by default): uses UDP for audio packets to improve audio performance.
- Personal vDisk (off by default, desktop OS only): usable with a master image.

FMA fact: a separate HDX 3D Pro VDA exists for GPU acceleration (3D OpenGL and DirectX; standard VDA does DirectX only). Resources can be assigned one-to-one (Passthrough) or shared across VMs (vGPU).

## Verwante notities

- [Delivery Controller server sizing and supported OS](delivery-controller-sizing.md)
- [Personal vDisks (PvD)](pvs-personal-vdisks-pvd.md)
- [Server VDA vs Desktop VDA: the often-overlooked new component](server-vda-vs-desktop-vda.md)
- [Single-User vs Multi-User VDI/DaaS](single-user-vs-multi-user-vdi-daas.md)
- [Two VDA types and the single-user vs multi-user ICA stack](two-vda-types-ica-stack-difference.md)
- [VDA license rules and Microsoft licensing nuances](vda-license-rules-microsoft-licensing.md)
- [The VDA: client-side component, services and registration](vda-overview-services-and-registration.md)
