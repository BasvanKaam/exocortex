---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [storefront, sizing, capacity, windows-server]
layer: reference
bron: inside-citrix-fma
---

# StoreFront server sizing and supported OSes

The number of simultaneous activities a StoreFront server can handle depends on the number of resources assigned to a user and overall user activity. Based on a 2-node StoreFront deployment, it can handle around 600 simultaneous activities per second at 80-85% CPU usage. Per-node specification:

- Processor: 4 vCPUs
- Memory: 4 GB RAM (minimum)
- Storage: 40 GB
- OS: Windows Server 2012 R2

Supported (tested) operating systems for StoreFront:
- Windows Server 2012 R2 Datacenter and Standard
- Windows Server 2012 Datacenter and Standard
- Windows Server 2008 R2 SP1 Datacenter, Enterprise and Standard

When running XenDesktop/XenApp 7.8 you need at least StoreFront 2.6 or higher.
