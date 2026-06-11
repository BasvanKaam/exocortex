---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-10
tags: [docker, windows, nano-server, containers]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Running Docker from Windows in 2015 required a Linux VM

How it worked then (April 2015). Docker binaries only ran on Linux, so to use Docker from an existing Windows environment you ran a virtual Linux machine hosting the Docker installation (e.g. via Boot2Docker) and drove it with the Windows Docker client (CLI), which was a native Windows application. The client could also manage Linux Docker hosts across the enterprise directly from Windows.

Forward-looking announcements at the time: Microsoft's 2016 Nano Server edition would introduce Windows-based containers into the Docker ecosystem, with an extremely small 'Nano' footprint touted as a security advantage. VMware had just announced Project Photon and Project Lightwave to add container support with extra security measures, and a future XenServer (Dundee) release was expected to manage Docker containers via a XenCenter supplemental pack.

*Bron: blogpost 'Containers? Docker? Docker on VMware. Docker on Windows. Docker on Citrix?' (2015-04-27), basvankaam.com.*

## Verwante notities

- [Stance: container concepts carry over from Docker/Linux to Windows](containers-concepts-durable-over-platform.md)
- [Windows Server 2016: native Windows Server containers vs Hyper-V containers](windows-server-2016-container-types.md)
