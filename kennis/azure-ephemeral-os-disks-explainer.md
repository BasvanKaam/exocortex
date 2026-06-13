---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [azure, ephemeral-disks, avd, wvd, storage, cost-optimization]
layer: reference
gedateerd: ja
bron: nerdio-blog
---

# Azure Ephemeral OS Disks (and Why They Fit Stateless AVD/WVD)

Ephemeral OS disks are stateless disk storage created on the VM's local storage (part of the VM cache), not written to Azure Blob storage. That gives lower latency and faster read/write than a normal managed disk.

Key facts (WVD/NMW era, captured around NMW 2.1.0):
- Free: no storage cost. You still pay for the VM compute and for any other disk types attached to the VM.
- Cannot be stopped/deallocated. Restarting is supported. This is the main constraint.
- Size is bounded by the VM cache size of the selected VM type (max 2 TB at the time). The golden/base image must fit in that cache size, otherwise pick a VM type with a larger cache.
- Disk size can only be set at VM creation, not changed afterwards.
- Only Managed disks supported. Supported VM families at the time: DSv1, DSv2, DSv3, Esv3, Fs, FsV2, GS, M.
- Supported in all regions worldwide.
- Starting a VM on an ephemeral disk is roughly 50 to 70 percent faster than a VM with a normal disk type.

Good fit for stateless pooled session desktops (multi-session), pooled single-user desktops, and RemoteApps, provided a solid profile solution like FSLogix and golden image(s) are in place.

*Bron: Nerdio-content 'What are Azure Ephemeral OS disks, why you should care, and how to use them with WVD' (Blogs).*

## Verwante notities

- [Turning the Ephemeral 'No Deallocate' Constraint Into a Win With Autoscaling](ephemeral-disk-constraint-vs-autoscaling.md)
- [Ephemeral OS disks: free, fast, stateless, and the deallocate caveat](ephemeral-os-disks-explained.md)
- [Ephemeral OS Disks for AVD: free, fast OS storage for stateless hosts](ephemeral-os-disks-for-avd.md)
- [IOPS, latency, and sizing storage for VDI workloads](iops-latency-and-sizing-storage-for-vdi.md)
- [How Nerdio makes Ephemeral OS Disks practical (JIT provisioning + image shrink)](nerdio-ephemeral-disks-jit-and-image-shrink.md)
- [Ephemeral OS Disks are underrated for stateless AVD](positie-ephemeral-os-disks-underrated.md)
