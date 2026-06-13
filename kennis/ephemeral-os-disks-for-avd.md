---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [avd, ephemeral-os-disks, storage, nerdio, autoscale, stateless, fslogix]
layer: reference
gedateerd: ja
bron: nerdio-blog
---

# Ephemeral OS Disks for AVD: free, fast OS storage for stateless hosts

Bas's explainer on using Ephemeral OS Disks to get free, fast OS storage for Azure Virtual Desktop. Product-specific, so treat as dated.

## What they are
- "Ephemeral" = short-lived. They suit **non-persistent / stateless** AVD workloads only: nothing is stored on the host between sessions. User settings still persist via FSLogix Profile Containers (the user profile), not the host disk.
- They cannot be used for persistent (stateful) personal desktops. Ideal fit: **multi-session** AVD hosts.
- Unlike a normal OS disk (attached to the VM, backed by Azure Blob storage), an Ephemeral OS Disk lives on the VM's **local storage**: nothing is written to Blob. Lower latency, faster reads/writes.

## Two placement options
Microsoft now supports two locations for the Ephemeral OS Disk:
1. **VM cache** (the original method, part of SSD storage cache).
2. **VM local temp disk** (added later).

Choice is made via the `DiffDiskPlacement` property. Not all VM types support Ephemeral OS Disks; among those that do, some support cache only, some temp only, some both. Microsoft documents which VMs are supported, and most popular AVD VM types are on the list.

## Advantages
- **100% free**: no charge for the storage at all.
- **Fast**: mounts local to the VM, nothing traverses the network, close to local physical-disk speed.
- Machines build and domain-join faster.
- All popular AVD VM types are supported.

## Disadvantages
- **Cannot be stopped/deallocated.** You always pay for the associated compute unless you fully destroy and later rebuild the machine.
- Not all VM types are supported.
- Not all disk features are supported: disk encryption, snapshots, backup, disk swap, site recovery and more (arguably unneeded for stateless workloads).
- Stopping = data loss (it's stateless by design); technically you must delete/redeploy rather than stop.

## OS disk and image size constraint
- Max Ephemeral OS Disk size is set by the VM type (e.g. 100 GB on some, 200 GB on others, per Microsoft docs).
- The disk must be large enough to hold the image. A default marketplace image is 128 GB and won't fit a 100 GB Ephemeral OS Disk. Options: pick a larger (more expensive) VM, or shrink the image (see Nerdio note).

## Native usage caveat
Natively this is not straightforward: you set `DiffDiskPlacement` via an API call, and you must destroy/recreate machines to avoid paying for compute 24/7. Hard to do well without automation.

*Bron: Nerdio-content 'Free OS disk storage for your Azure Virtual Desktop hosts' (Blogs).*

## Verwante notities

- [Azure Ephemeral OS Disks (and Why They Fit Stateless AVD/WVD)](azure-ephemeral-os-disks-explainer.md)
- [Azure GPU VMs: NVIDIA vs AMD NVv4, licensing and partitioning](azure-gpu-vms-licensing-and-nvv4-partitioning.md)
- [Turning the Ephemeral 'No Deallocate' Constraint Into a Win With Autoscaling](ephemeral-disk-constraint-vs-autoscaling.md)
- [Ephemeral OS disks: free, fast, stateless, and the deallocate caveat](ephemeral-os-disks-explained.md)
- [IOPS, latency, and sizing storage for VDI workloads](iops-latency-and-sizing-storage-for-vdi.md)
- [How Nerdio makes Ephemeral OS Disks practical (JIT provisioning + image shrink)](nerdio-ephemeral-disks-jit-and-image-shrink.md)
- [Ephemeral OS Disks are underrated for stateless AVD](positie-ephemeral-os-disks-underrated.md)
