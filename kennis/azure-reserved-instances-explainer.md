---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [azure, reserved-instances, cost-optimization, wvd, avd]
layer: reference
gedateerd: ja
bron: nerdio-blog
---

# Azure Reserved Instances: How They Work and When to Use Them

Reserved Instances (RI) = a 1- or 3-year commitment to rent a number of VMs in exchange for a discount on Azure compute (over 70% in some cases). More expensive VM types generally carry a bigger discount.

Key mechanics (WVD era, verify current Azure terms before reuse):
- There is a 'tipping point' per VM type: how many hours/day the VM runs determines whether a 1/3-year commit beats Pay-as-you-go. Compare with the Azure Calculator or a tool like vmchooser.
- Bas's advice: run the environment first, then apply RI later, once you know the real average run-hours, unless you are already certain.
- Normal VM types can now be paid monthly (no longer upfront-only). At the time, RIs applied to WVD still appeared to require upfront payment in the calculator.
- Early exit: pay a fine of 12% of the remaining contract value; the rest is refunded. (Worked example: 3-yr contract at 1000/yr, 1 year left = 1000, fine = 120, you get 880 back.) Note at time of writing there was temporarily no cancellation fee.
- Per Microsoft: you can exchange a reservation for another of the same type, or refund up to $50,000 USD in a rolling 12-month window. Same-type only (no VM-for-SQL-PaaS swap). VM size changes mid-contract are possible, even automated.

WVD/AVD use-cases for RI: base-capacity hosts that run most of the time, 24x7 hostpools, domain controllers, print/file servers, databases, web servers, and reserved DR capacity. Steady, predictable workloads.

*Bron: Nerdio-content 'What you need to know about Azure Reserved Instances, Azure Hybrid Benefit and WVD' (Blogs).*

## Verwante notities

- [Auto-scale first, then reserve the residual](auto-scale-before-reserved-instances.md)
- [Autoscaling Can Beat Reserved Instances for Variable WVD Workloads](autoscaling-vs-reserved-instances-stance.md)
- [Azure cost levers: CSP, right-sizing, promos and Reserved Instances](azure-cost-levers-csp-vm-sizing-ri.md)
- [Azure Hybrid Benefit and the Linux-Pricing 'Fun Fact'](azure-hybrid-benefit-explainer.md)
- [Azure On-demand Capacity Reservation Cheat Sheet](azure-on-demand-capacity-reservation-cheat-sheet.md)
- [B-series burstable VMs: the CPU-credit model and when to use them](b-series-burstable-vms-explained.md)
- [For steady WVD workloads, reserved instances almost always win](reserved-instances-almost-always-cheaper-position.md)
- [Reserved Instances Do Not Guarantee Compute Availability](reserved-instances-do-not-guarantee-compute.md)
- [Estimating WVD cost for under-100-user environments with the Azure calculator](wvd-azure-calculator-small-environment-method.md)
