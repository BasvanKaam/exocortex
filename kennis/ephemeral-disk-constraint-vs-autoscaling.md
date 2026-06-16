---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [nerdio, autoscale, ephemeral-disks, cost-optimization, avd]
layer: reference
gedateerd: ja
bron: nerdio-blog
---

# Turning the Ephemeral 'No Deallocate' Constraint Into a Win With Autoscaling

The big con of ephemeral disks is that the VM cannot be stopped/deallocated, only restarted. Bas's argument: this con disappears under Nerdio autoscaling, because autoscaling adds and removes whole VMs rather than deallocating them, while retaining the important identity (machine name, IP address, DNS, and Active Directory records).

So instead of shutting a host down to save cost, you delete it and recreate it from the image on demand. You can scale all the way down to zero active machines, which is exactly what you need for cost control when the underlying disks can't be deallocated.

Net effect Bas claims: free disk storage + autoscaling savings + lower latency / faster read-write = a 'win-win-win' for cost and user experience.

*Bron: Nerdio-content 'What are Azure Ephemeral OS disks, why you should care, and how to use them with WVD' (Blogs).*

## Verwante notities

- [Azure Ephemeral OS Disks (and Why They Fit Stateless AVD/WVD)](azure-ephemeral-os-disks-explainer.md)
- [Ephemeral OS disks: free, fast, stateless, and the deallocate caveat](ephemeral-os-disks-explained.md)
- [Ephemeral OS Disks for AVD: free, fast OS storage for stateless hosts](ephemeral-os-disks-for-avd.md)
- [Nerdio autoscaling engine: pooled hostpool scaling logic](nerdio-autoscaling-engine-pooled-hostpools.md)
- [How Nerdio makes Ephemeral OS Disks practical (JIT provisioning + image shrink)](nerdio-ephemeral-disks-jit-and-image-shrink.md)
- [Nerdio Manager for WVD: the cost-saving levers (WVD era)](nmw-cost-saving-levers-overview.md)
- [Ephemeral OS Disks are underrated for stateless AVD](positie-ephemeral-os-disks-underrated.md)
