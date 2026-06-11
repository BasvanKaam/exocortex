---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-10
tags: [Azure, reserved-instances, cost, opex]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Reserved Instances: 12% early-exit fine and monthly payment

How it worked in 2020. If you cancel an Azure Reserved Instance early, you pay a 12% fine over the remainder of the contract (the unused consumption); the rest is refunded. Doing the math, a 1- or 3-year reservation is almost always cheaper than pay-per-use.

Reserved Instances used to require upfront payment (capex), but by 2020 you could pay monthly (opex) for normal VM types, removing the old capex hurdle. (Note: at the time, RIs applied to WVD in the calculator still appeared to require upfront payment.)

*Bron: blogpost 'How to: Calculating costs for smaller WVD environments using the Azure Calculator' (2020-06-24), basvankaam.com.*

## Verwante notities

- [M365 E3 already entitles you to AHU for WVD](ahu-entitlement-via-m365-e3.md)
- [Autoscaling can beat Reserved Instances, and pairs with them](autoscaling-vs-reserved-instances.md)
- [Reserved, Scheduled and Spot instances as AWS cost levers](aws-instance-purchasing-models-cost.md)
- [How Azure Reserved Instances and Hybrid Benefit work](azure-ri-ahb-mechanics.md)
- [WVD session hosts are charged at Linux compute rates](wvd-charged-at-linux-rates.md)
- [Cheap WVD lab: de-allocate VMs, pay only for storage](wvd-lab-cost-deallocate-vms.md)
