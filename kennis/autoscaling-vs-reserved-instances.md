---
type: positie
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-10
tags: [autoscaling, reserved-instances, WVD, Nerdio, cost, opinion]
bron: basvankaam-blog
---

# Autoscaling can beat Reserved Instances, and pairs with them

Bas's position (July 2020): instead of committing to Reserved Instances, autoscaling can reduce monthly/yearly compute cost, sometimes more attractively than RIs, with no separate contract. He claims Nerdio's autoscaling can cut WVD host costs by over 70% and shows min/max cost instantly once configured.

But he doesn't frame it as either/or. RIs are the right tool for steady, predictable, near-24x7 workloads: base-capacity hosts that stay on, domain controllers, print/file servers, databases, webservers, DR standby capacity. So the recommended model is RIs for the always-on base layer plus autoscaling for the variable layer, usually combined with AHB. 'Steady, predictable workloads, that's what RI's are made for.'

*Bron: blogpost 'What you need to know about Azure Reserved Instances, AHB and WVD' (2020-07-07), basvankaam.com.*

## Verwante notities

- [M365 E3 already entitles you to AHU for WVD](ahu-entitlement-via-m365-e3.md)
- [Reserved, Scheduled and Spot instances as AWS cost levers](aws-instance-purchasing-models-cost.md)
- [Estimating small WVD environments in the Azure calculator](azure-calculator-small-wvd-trick.md)
- [How Azure Reserved Instances and Hybrid Benefit work](azure-ri-ahb-mechanics.md)
- [Ephemeral disks' biggest drawback disappears with the right autoscaler](ephemeral-disks-cons-as-pros.md)
- [Indicative cost overview: split the totals, show the assumptions, never call it a quote](indicative-cost-overview-method-assumptions-and-reserved-instances.md)
- [How Nerdio's WVD autoscale worked: triggers, base/burst capacity, graceful drain](nerdio-autoscale-mechanics-2020.md)
- [Microsoft's WVD power scripts are not real autoscaling](nerdio-vs-microsoft-power-management-scripts.md)
- [Reserved Instances: 12% early-exit fine and monthly payment](reserved-instance-early-exit-fine.md)
- [Static vs dynamic host pools and autoscaling (Nerdio)](static-vs-dynamic-hostpools-nerdio.md)
- [WVD session hosts are charged at Linux compute rates](wvd-charged-at-linux-rates.md)
