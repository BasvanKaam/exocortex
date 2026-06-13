---
type: positie
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [positie, ephemeral-os-disks, avd, cost-optimization]
bron: nerdio-blog
---

# Ephemeral OS Disks are underrated for stateless AVD

Bas's stance: Ephemeral OS Disks have always been a topic of discussion but haven't gotten the attention they deserve. For stateless, multi-session AVD they offer free, fast OS storage and are simpler to set up and manage than people assume. He won't claim they fit every use case, but more teams should try them. The standard cost objections (no stop/deallocate, image won't fit) are real but solvable with autoscale just-in-time provisioning and image shrink.

*Bron: Nerdio-content 'Free OS disk storage for your Azure Virtual Desktop hosts' (Blogs).*

## Verwante notities

- [Azure Ephemeral OS Disks (and Why They Fit Stateless AVD/WVD)](azure-ephemeral-os-disks-explainer.md)
- [Turning the Ephemeral 'No Deallocate' Constraint Into a Win With Autoscaling](ephemeral-disk-constraint-vs-autoscaling.md)
- [Ephemeral disks' biggest drawback disappears with the right autoscaler](ephemeral-disks-cons-as-pros.md)
- [Ephemeral OS disks: free, fast, stateless, and the deallocate caveat](ephemeral-os-disks-explained.md)
- [Ephemeral OS Disks for AVD: free, fast OS storage for stateless hosts](ephemeral-os-disks-for-avd.md)
- [How Nerdio makes Ephemeral OS Disks practical (JIT provisioning + image shrink)](nerdio-ephemeral-disks-jit-and-image-shrink.md)
