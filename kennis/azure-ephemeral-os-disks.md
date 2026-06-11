---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-10
tags: [Azure, ephemeral-disks, WVD, stateless, storage]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Azure Ephemeral OS disks for stateless WVD workloads

How it worked in 2020. Ephemeral OS disks are stateless storage created on the VM's local storage as part of the VM cache; they are not written to Azure Blob storage. This gives lower latency and faster read/write, making them ideal for stateless workloads.

Key properties:
- Free: no storage charge (you still pay for the VM's compute and any other attached disks).
- Cannot be stopped/deallocated; restart is supported.
- Sized from the VM cache, max 2 TB. If the cache is too small to hold your golden image, pick a VM type with a larger cache. Disk size can only be set at VM creation, not changed afterwards.
- Supported VM types (2020): DSv1, DSv2, DSv3, Esv3, Fs, FsV2, GS, M. Only Managed disks supported. Available in all regions.
- Starting a VM on an ephemeral disk is 50-70% faster than on a 'normal' disk type.

Good fit for WVD pooled session desktops (multi-session / Windows 10), pooled single-user desktops, and RemoteApps, paired with a solid profile solution like FSLogix and one or more golden images.

*Bron: blogpost 'What are Azure Ephemeral disks, how to use them with WVD, and why care?' (2020-07-01), basvankaam.com.*

## Verwante notities

- [Azure Files storage redundancy: LRS, ZRS, GRS](azure-files-storage-redundancy-lrs-zrs-grs.md)
- [How Azure Reserved Instances and Hybrid Benefit work](azure-ri-ahb-mechanics.md)
- [The 'big bad image' problem: why everything in the base image hurts](big-bad-base-image-problems.md)
- [Ephemeral disks' biggest drawback disappears with the right autoscaler](ephemeral-disks-cons-as-pros.md)
- [How Nerdio's WVD autoscale worked: triggers, base/burst capacity, graceful drain](nerdio-autoscale-mechanics-2020.md)
- [Cheap WVD lab: de-allocate VMs, pay only for storage](wvd-lab-cost-deallocate-vms.md)
- [FSLogix Profile Containers as the WVD profile standard (2019)](wvd-profiles-fslogix-azure-files-2019.md)
