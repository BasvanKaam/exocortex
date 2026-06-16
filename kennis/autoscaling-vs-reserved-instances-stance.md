---
type: positie
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [nerdio, autoscale, reserved-instances, cost-optimization, positie]
bron: nerdio-blog
---

# Autoscaling Can Beat Reserved Instances for Variable WVD Workloads

Bas's stance: RIs are not the only cost lever, and for variable WVD workloads they are often not the best one. Autoscaling can reduce monthly/yearly compute cost without any separate contract, and for WVD hosts the Nerdio autoscaling mechanism can cut costs by over 70%, to a point where it can be more interesting than RIs.

His recommended pattern is to split the workload:
- Use RIs (plus AHB where licenses allow) for the base-capacity machines that run most of the time.
- Use autoscaling for the variable layer that flexes with users through the day.

He also notes that in roughly 75% of cases or more, RIs will save money, and a combination of RIs and AHB is usually the strongest pairing, except for B-series VMs where you should do the math.

*Bron: Nerdio-content 'What you need to know about Azure Reserved Instances, Azure Hybrid Benefit and WVD' (Blogs).*

## Verwante notities

- [Auto-scale first, then reserve the residual](auto-scale-before-reserved-instances.md)
- [Five (plus RI) AVD cost-reduction options](avd-five-cost-reduction-options.md)
- [Azure Hybrid Benefit and the Linux-Pricing 'Fun Fact'](azure-hybrid-benefit-explainer.md)
- [Azure Reserved Instances: How They Work and When to Use Them](azure-reserved-instances-explainer.md)
- [B-series burstable VMs: the CPU-credit model and when to use them](b-series-burstable-vms-explained.md)
- [Nerdio autoscaling engine: pooled hostpool scaling logic](nerdio-autoscaling-engine-pooled-hostpools.md)
- [Hide the Complexity, Broaden the Line Between UX and Cost](position-hide-complexity-broaden-the-line.md)
- [Reserved Capacity still leaves you guessing; autoscale is the better answer](position-reserved-capacity-vs-autoscale.md)
- [For steady WVD workloads, reserved instances almost always win](reserved-instances-almost-always-cheaper-position.md)
