---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-10
tags: [containers, windows-server-2016, docker, hyper-v, isolation]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Windows Server 2016: native Windows Server containers vs Hyper-V containers

How it was introduced with Windows Server 2016 Technical Preview 3 (2015).

Two container types:
- **Native Windows Server containers** (available in TP3): run on a physical or virtualised Server 2016 host and interact with the underlying OS kernel the same way Docker containers do. They share a great deal of the underlying Windows kernel subsystems and devices with all other containers on the host.
- **Hyper-V containers** (announced for TP4): each container gets its own copy of the Windows kernel, isolating it from other containers for additional isolation and security.

Both types use the same management APIs, tools and image formats. The runtime type is chosen at start time, so an image built for one can be deployed as the other by specifying the runtime flag, no changes needed. The main difference is isolation.

This differs from traditional application virtualisation like App-V, which offers full isolation in a private bubble. A native Windows Server container looks sandboxed to the app but still shares kernel subsystems. You cannot run Linux containers on Windows or vice versa (different kernel APIs), but the goal was one unified Docker toolset to manage both. Getting started required a Core installation, at least 10 GB free disk, and a base container OS image (setup via aka.ms/setupcontainers script or Install-WindowsFeature -name Containers).

*Bron: blogpost 'Windows Server 2016 containers: native vs Hyper-V containers' (2015-08-20), basvankaam.com.*

## Verwante notities

- [Framing: keep application layering and application virtualization distinct](app-layering-not-app-virtualization.md)
- [Citrix's native options still lag third-party containers (May 2018)](citrix-still-behind-third-party-containers-2018.md)
- [Stance: container concepts carry over from Docker/Linux to Windows](containers-concepts-durable-over-platform.md)
- [Docker fundamentals: namespaces, cgroups, images and layers](docker-inner-workings-2015.md)
- [Running Docker from Windows in 2015 required a Linux VM](docker-on-windows-2015-state.md)
- [Containers hold great potential but aren't easy out of the box](stance-docker-promise-vs-complexity.md)
- [Windows Server 2019 at announcement: LTSC/SAC, RDSH question, RDmi](windows-server-2019-ltsc-sac-rdmi.md)
