---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [mcs, xenserver, hyper-v, nfs, thin-provisioning]
layer: reference
bron: inside-citrix-fma
---

# MCS supported hypervisor storage and thin provisioning limits

For MCS you can use NFS for XenServer and ESXi, or Clustered Shared Volumes for Hyper-V. At the time of writing there is no thin provisioning on XenServer with block-based storage (interesting block-based storage developments were on their way in the XenServer Tech Preview a.k.a. Dundee).

MCS with Hyper-V local storage is also an option: configure a cluster without shared storage and a copy of the master image is placed on a local drive (C:\, D:\, etc.).

Citrix used to recommend NFS exclusively with MCS, but that was geared toward XenServer's inability to thin provision block-based storage rather than anything else. NFS is more straightforward to configure and maintain, but block-based storage with MCS is also supported and used in many production environments.
