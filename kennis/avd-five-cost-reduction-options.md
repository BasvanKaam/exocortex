---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [avd, nerdio, autoscale, fslogix, kosten, dated]
layer: reference
gedateerd: ja
bron: nerdio-blog
---

# Five (plus RI) AVD cost-reduction options

A stacked, ordered framework Bas uses to walk a typical MSP-sized AVD deployment from unoptimized to ~68% cheaper. Each option layers on top of the previous one. Sample case: 32 heavy users, E4s_v4 hosts, P10 128GB OS disks, 20GB FSLogix profiles on Azure Files Premium, ~50 work hours/week.

1. **VM power management** — VMs only need to run during the ~50 of 168 weekly hours users actually work. Auto-scaling on/off cuts compute by ~70%, the single biggest win. Storage still bills while VMs are off.
2. **Burst / just-in-time provisioning** — keep half the hosts as base capacity, create and delete the other half on demand. Deleted VMs stop billing their attached OS disks. Bonus: rebuilding from the latest image daily keeps hosts pristine and avoids configuration drift (includes re-joining the domain).
3. **OS disk auto-scale** — base-capacity VMs keep a Premium SSD (P10) while running for performance, but swap to a cheap Standard HDD when stopped, then swap back on start. HDD is ~75% cheaper than Premium SSD; the swap is near-instant.
4. **Shrink the OS disk from 128GB to 64GB** — Azure Gallery Win10/11 images ship a 128GB disk that is mostly empty. In multi-session pooled (non-persistent) deployments nothing is saved to C: (user data redirects to FSLogix) and hosts rebuild from image, so there is no disk growth. A scripted action shrinks to 64GB, halving OS-disk storage.
5. **FSLogix profile whitespace reduction + storage auto-scale** — FSLogix containers are thin-provisioned VHD(X) files that grow but never shrink. A scheduled whitespace-removal process reclaims ~50%. Because Azure Files Premium bills on provisioned quota (not actual usage), a separate storage auto-scale engine adjusts the quota up/down based on free space and measured latency.

6 (coming, RI Analytics). **Reserved Instances on top of auto-scale** — first auto-scale to shrink the number of compute hours, then reserve only the cores still needed for those remaining hours. Reserving everything makes auto-scale pointless; reserving the residual after auto-scale combines both savings.

Key insight: auto-scaling PAYG typically saves more than blanket RIs, so apply auto-scale first and reserve the leftover, not the whole fleet.

*Bron: Nerdio-content 'Significantly lowering your costs for Azure Virtual Desktop using these 5 cost reduction options' (Blogs).*

## Verwante notities

- [Auto-scale first, then reserve the residual](auto-scale-before-reserved-instances.md)
- [Autoscaling Can Beat Reserved Instances for Variable WVD Workloads](autoscaling-vs-reserved-instances-stance.md)
- [AVD cost-component breakdown](avd-cost-component-breakdown.md)
- [AVD Cost Modelling: Modeler + User Cost Attribution](avd-cost-modelling-modeler-and-cost-attribution.md)
- [Nerdio Manager storage autoscale for Azure Files Premium](nerdio-azure-files-premium-autoscale.md)
- [Nerdio Cost-Optimization Levers (Bas's Assessment Method)](nerdio-cost-optimization-levers.md)
- [How Nerdio makes Ephemeral OS Disks practical (JIT provisioning + image shrink)](nerdio-ephemeral-disks-jit-and-image-shrink.md)
