---
type: positie
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [avd, reserved-instances, autoscale, cost]
bron: nerdio-blog
---

# Auto-scale first, then reserve the residual

Bas's stance on Reserved Instances: reserving all or almost all session-host capacity is the default people reach for, but it is the wrong order. Auto-scaling PAYG VMs typically saves more than RIs because most hosts sit idle outside the ~50 working hours per week. The efficient approach is to auto-scale first to cut the number of compute hours, then reserve only the cores still needed for the remaining hours. Reserving everything upfront makes auto-scaling pointless. Done in the right order, you stack a ~60-70% compute reduction from auto-scale with a further reservation discount on the residual.

*Bron: Nerdio-content 'Significantly lowering your costs for Azure Virtual Desktop using these 5 cost reduction options' (Blogs).*

## Verwante notities

- [Autoscaling Can Beat Reserved Instances for Variable WVD Workloads](autoscaling-vs-reserved-instances-stance.md)
- [Five (plus RI) AVD cost-reduction options](avd-five-cost-reduction-options.md)
- [Azure Reserved Instances: How They Work and When to Use Them](azure-reserved-instances-explainer.md)
- [Nerdio Cost-Optimization Levers (Bas's Assessment Method)](nerdio-cost-optimization-levers.md)
- [Reserved Capacity still leaves you guessing; autoscale is the better answer](position-reserved-capacity-vs-autoscale.md)
- [Shutting Down Reserved Machines Saves Nothing on Compute](position-shutting-down-reserved-machines-saves-nothing.md)
- [For steady WVD workloads, reserved instances almost always win](reserved-instances-almost-always-cheaper-position.md)
- [Reserved Instances Do Not Guarantee Compute Availability](reserved-instances-do-not-guarantee-compute.md)
