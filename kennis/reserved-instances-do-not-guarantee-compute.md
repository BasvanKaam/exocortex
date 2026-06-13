---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [azure, reserved-instances, capacity, cost-optimization]
layer: reference
gedateerd: ja
bron: nerdio-content
---

# Reserved Instances Do Not Guarantee Compute Availability

A point Bas hammers because it is widely misunderstood. Per Microsoft, Azure Reserved VM Instances offer *prioritized* capacity but do not *guarantee* that capacity will be available for your VMs. The priority is for a VM SKU in a region; it is not reserved for a specific availability set or scale set.

Key clarifications Bas makes:
- RIs are **not** actual reserved virtual machines. They are a commitment to a number and type of CPU cores, applied against the machine families you deploy where there is a match.
- With RIs and on-demand reserved capacity, compute is paid for up front. Shutting machines down (manually or via scaling) does **not** lower the compute cost. The disk/storage is the exception.
- On-demand reserved capacity *does* guarantee availability and carries discounts, but again shutdown does not reduce its compute cost.
- At time of writing there is no penalty for handing RIs back to Microsoft (he flags this may change).

**Utilization test for whether an RI even pays off:** if a VM runs and is used 60%+ of the available hours in a month, an RI makes sense on cost. Below that, the RI still buys prioritized (not guaranteed) capacity but does not lower cost, and you are over-spending. Use a tool such as Citrix Director to measure real usage, especially on single-session VMs, before committing.

The strategy that follows: identify idle reserved cores, hand back the genuine excess, keep a deliberate slice as a fallback, and consider combining reserved capacity with pay-per-use machines under Nerdio autoscale. Azure Capacity Extender (starting additional machine types) is an optional add to this.

See also: nerdio-cost-optimization-levers.

*Bron: Nerdio-content 'MCS' ((root)).*

## Verwante notities

- [Auto-scale first, then reserve the residual](auto-scale-before-reserved-instances.md)
- [Azure On-demand Capacity Reservation Cheat Sheet](azure-on-demand-capacity-reservation-cheat-sheet.md)
- [Azure Reserved Instances: How They Work and When to Use Them](azure-reserved-instances-explainer.md)
- [Nerdio Cost-Optimization Levers (Bas's Assessment Method)](nerdio-cost-optimization-levers.md)
- [Shutting Down Reserved Machines Saves Nothing on Compute](position-shutting-down-reserved-machines-saves-nothing.md)
- [For steady WVD workloads, reserved instances almost always win](reserved-instances-almost-always-cheaper-position.md)
