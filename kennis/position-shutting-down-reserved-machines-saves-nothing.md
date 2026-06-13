---
type: positie
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [azure, reserved-instances, cost-optimization, positie]
bron: nerdio-content
---

# Shutting Down Reserved Machines Saves Nothing on Compute

Bas's stance: when an estate is fully on reserved instances or on-demand reserved capacity, the usual lever everyone reaches for, shutting machines down and applying scaling, does nothing for compute cost because compute is paid up front. The only compute saving comes from actually reducing what is reserved or moving part of the estate to pay-per-use under autoscale. The shutdown lever only buys you the disk/storage swap. If you believe scaling alone is cutting your bill on a 100%-reserved estate, you are mistaken, and if your VMs run under ~60% utilization you are over-spending on the reservations themselves.

See also: reserved-instances-do-not-guarantee-compute, nerdio-cost-optimization-levers.

*Bron: Nerdio-content 'MCS' ((root)).*

## Verwante notities

- [Auto-scale first, then reserve the residual](auto-scale-before-reserved-instances.md)
- [Azure On-demand Capacity Reservation Cheat Sheet](azure-on-demand-capacity-reservation-cheat-sheet.md)
- [Nerdio Cost-Optimization Levers (Bas's Assessment Method)](nerdio-cost-optimization-levers.md)
- [Reserved Capacity still leaves you guessing; autoscale is the better answer](position-reserved-capacity-vs-autoscale.md)
- [For steady WVD workloads, reserved instances almost always win](reserved-instances-almost-always-cheaper-position.md)
- [Reserved Instances Do Not Guarantee Compute Availability](reserved-instances-do-not-guarantee-compute.md)
