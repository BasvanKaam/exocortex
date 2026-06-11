---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-10
tags: [docker, containers, linux, devops]
layer: reference
gedateerd: nee
bron: basvankaam-blog
---

# Docker fundamentals: namespaces, cgroups, images and layers

Docker automates deployment of applications inside containers using OS-level virtualization on Linux. Core mechanics:

- Containers use Linux kernel features: kernel namespaces isolate a container's view of the OS (namespaces are what actually create the container), and cgroups (control groups) limit and control CPU, memory, IO and certain network characteristics.
- Parts: a server daemon on the Linux host; a CLI (Linux and Windows distributions) to build/run/manage containers; an image index (public or private repository of ready-to-use images).
- Elements: containers (kernel-level features managing the app on top), images (the base-OS-like layer that forms and runs inside the container), and Dockerfiles (a series of commands automating image creation).
- Layering: images are built in layers, one on top of another, keeping them lightweight. Updating an app builds a new layer rather than rebuilding the whole image, so you distribute only the changed layer, not a new full image. This also makes snapshots and rollbacks easy.

Trade-offs noted: containers launch in seconds, are portable across physical/virtual/cloud (only dependency is Docker installed on the host), achieve higher density, and pair well with DevOps. Downsides: less isolation than a full VM, and multiple containers share the same underlying kernel, which is a potential security surface since not all kernel subsystems are isolated.

*Bron: blogpost 'Containers? Docker? Docker on VMware. Docker on Windows. Docker on Citrix?' (2015-04-27), basvankaam.com.*

## Verwante notities

- [Citrix Octoblu: an everything-is-a-node IoT platform](citrix-octoblu-architecture.md)
- [Stance: container concepts carry over from Docker/Linux to Windows](containers-concepts-durable-over-platform.md)
- [Windows Server 2016: native Windows Server containers vs Hyper-V containers](windows-server-2016-container-types.md)
