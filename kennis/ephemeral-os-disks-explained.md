---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-11
tags: [azure, ephemeral-os-disk, non-persistent, cost-optimization]
layer: reference
gedateerd: nee
bron: nerdio-blog
---

# Ephemeral OS disks: free, fast, stateless, and the deallocate caveat

Bas's explainer on Ephemeral OS disks, especially relevant for stateless / non-persistent workloads.

What they are: a form of stateless disk storage created on the VM's local storage (part of the VM cache), not written to Azure Blob storage. That gives lower latency and faster read/write.

Pros: they are free, you are not charged for the OS-disk storage. (You still pay for the VM compute the disk runs on, and for any other disks you attach.)

Biggest drawback: Ephemeral disks cannot be stopped/deallocated. Restarting is supported, stop-deallocate is not. His point: combined with an autoscale engine this drawback mostly disappears, because autoscale can create new VMs from scratch in minutes, pre-stage machines, monitor and auto-heal, and fully remove/deallocate VMs when no longer needed, so you get the storage savings without the persistence penalty. 'You get the best of both worlds.'

*Bron: Nerdio-content 'How to save money on the Microsoft Azure list price' (Blogs).*

## Verwante notities

- [Azure cost levers: CSP, right-sizing, promos and Reserved Instances](azure-cost-levers-csp-vm-sizing-ri.md)
- [Azure Ephemeral OS disks for stateless WVD workloads](azure-ephemeral-os-disks.md)
- [Azure Ephemeral OS Disks (and Why They Fit Stateless AVD/WVD)](azure-ephemeral-os-disks-explainer.md)
- [B-series burstable VMs: the CPU-credit model and when to use them](b-series-burstable-vms-explained.md)
- [Turning the Ephemeral 'No Deallocate' Constraint Into a Win With Autoscaling](ephemeral-disk-constraint-vs-autoscaling.md)
- [Ephemeral OS Disks for AVD: free, fast OS storage for stateless hosts](ephemeral-os-disks-for-avd.md)
- [How Nerdio makes Ephemeral OS Disks practical (JIT provisioning + image shrink)](nerdio-ephemeral-disks-jit-and-image-shrink.md)
- [Ephemeral OS Disks are underrated for stateless AVD](positie-ephemeral-os-disks-underrated.md)
