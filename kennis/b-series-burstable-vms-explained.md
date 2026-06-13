---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-11
tags: [azure, b-series, vm, cost-optimization]
layer: reference
gedateerd: nee
bron: nerdio-blog
---

# B-series burstable VMs: the CPU-credit model and when to use them

Bas's explainer on Azure B-series 'burstable' VMs.

Use case: non-CPU-intensive workloads (domain controllers, file servers, web servers). They cost roughly 50% of an equivalently sized Ds-series VM (the family typically used for WVD session hosts).

Why cheaper: Azure imposes a quota on how much of the total CPU cores can be used, usually a fraction of the total available CPU. Every second the VM uses less than its quota it banks credits. Banked credits can be spent to burst up to the full available CPUs when needed; while bursting the VM consumes banked credits. Once credits run out, CPU is throttled back down to the pre-defined quota.

Practical framing he gives: for roughly the price of a Ds-series VM you can get a B-series with double the CPUs and double the RAM, but only for non-intensive CPU workloads. Do not put sustained-load workloads on burstable VMs.

*Bron: Nerdio-content 'How to save money on the Microsoft Azure list price' (Blogs).*

## Verwante notities

- [Autoscaling Can Beat Reserved Instances for Variable WVD Workloads](autoscaling-vs-reserved-instances-stance.md)
- [Azure cost levers: CSP, right-sizing, promos and Reserved Instances](azure-cost-levers-csp-vm-sizing-ri.md)
- [Azure Hybrid Benefit and the Linux-Pricing 'Fun Fact'](azure-hybrid-benefit-explainer.md)
- [Azure Reserved Instances: How They Work and When to Use Them](azure-reserved-instances-explainer.md)
- [Cloud cost-optimization levers](cloud-cost-optimization-levers.md)
- [Ephemeral OS disks: free, fast, stateless, and the deallocate caveat](ephemeral-os-disks-explained.md)
- [Nerdio non-technical cost levers](nerdio-non-technical-cost-levers.md)
- [Bas on sizing: there is no 'one size fits all', and don't overdo it](sizing-no-one-size-fits-all.md)
- [Size virtual desktops by testing, not by general guidelines](wvd-sizing-test-dont-trust-guidelines.md)
