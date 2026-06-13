---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [nerdio, ephemeral-os-disks, autoscale, just-in-time, scripted-actions, avd]
layer: reference
gedateerd: ja
bron: nerdio-blog
---

# How Nerdio makes Ephemeral OS Disks practical (JIT provisioning + image shrink)

The two Nerdio capabilities Bas points to for turning Ephemeral OS Disk cons into pros. Product-specific, treat as dated.

## Selecting Ephemeral OS Disks (complexity hidden)
When creating/configuring a host pool, pick your VM type; if it supports an Ephemeral OS Disk you can filter for it and select it from the same dropdown as any other disk type. Nerdio hides the native `DiffDiskPlacement`/API complexity.

## Just-in-time provisioning (solves the 24/7 compute cost)
The autoscale engine's just-in-time provisioning builds machines from scratch and fully removes them when no longer used:
- Pre-build any number of machines at a set time (e.g. 07:00-08:00).
- Autoscale builds more during the day as user load increases.
- Optionally keep one or more running for out-of-hours users.
- At end of day it fully removes machines, with selectable "aggressiveness" settings.
Result: free, fast Ephemeral storage with no 24/7 compute cost, you only pay for what's consumed.

## Image shrink (solves the disk-size constraint)
Via the Scripted Actions library, Nerdio can shrink a 128 GB image down to 64 GB, so you can run a smaller, cheaper VM and still apply your image of choice rather than jumping to a pricier VM with a larger Ephemeral OS Disk.

*Bron: Nerdio-content 'Free OS disk storage for your Azure Virtual Desktop hosts' (Blogs).*

## Verwante notities

- [Five (plus RI) AVD cost-reduction options](avd-five-cost-reduction-options.md)
- [Azure Ephemeral OS Disks (and Why They Fit Stateless AVD/WVD)](azure-ephemeral-os-disks-explainer.md)
- [Turning the Ephemeral 'No Deallocate' Constraint Into a Win With Autoscaling](ephemeral-disk-constraint-vs-autoscaling.md)
- [Ephemeral OS disks: free, fast, stateless, and the deallocate caveat](ephemeral-os-disks-explained.md)
- [Ephemeral OS Disks for AVD: free, fast OS storage for stateless hosts](ephemeral-os-disks-for-avd.md)
- [Nerdio autoscaling engine: pooled hostpool scaling logic](nerdio-autoscaling-engine-pooled-hostpools.md)
- [What Nerdio Scripted Actions are](nmw-scripted-actions-explainer.md)
- [Ephemeral OS Disks are underrated for stateless AVD](positie-ephemeral-os-disks-underrated.md)
