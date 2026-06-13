---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-10
tags: [Azure, reserved-instances, AHB, licensing, cost]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# How Azure Reserved Instances and Hybrid Benefit work

How it worked in 2020.

Reserved Instances (RI): a 1- or 3-year commitment to rent a number of VMs in exchange for a discount on Azure compute, up to ~70% on pricier VM types. There is a per-VM-type 'tipping point' where RIs stop beating Pay-as-you-go, driven mainly by how many hours the VM runs. Advice: run the environment first, then apply 1-/3-year optimisation once you know average uptime. RIs could be paid monthly by 2020 (was upfront/capex before), except RIs applied to WVD still appeared to require upfront payment.

Early exit: 12% fine on the remainder of the contract, rest refunded. Example: 3-year x 1000/year, 1 year left = 1000 remaining; fine 120, refund 880. (At time of writing there was temporarily no cancellation fee.) You can also exchange a reservation for another of the same type (no VM-for-SQL-PaaS swaps), across regions, and change VM sizes mid-contract. Refunds capped at $50,000 USD in a 12-month rolling window.

Azure Hybrid Benefit (AHB): bring an owned Windows Server and/or SQL license (with Software Assurance, or via a CSP subscription) into Azure so you don't pay for the Windows/SQL license on Azure. Windows Server Standard licenses move to the cloud VM and can no longer be used on-prem (up to two VMs in Azure, max 16 cores); Datacenter licenses allow up to two VMs in Azure plus any number on-prem on Hyper-V.

*Bron: blogpost 'What you need to know about Azure Reserved Instances, AHB and WVD' (2020-07-07), basvankaam.com.*

## Verwante notities

- [M365 E3 already entitles you to AHU for WVD](ahu-entitlement-via-m365-e3.md)
- [Autoscaling can beat Reserved Instances, and pairs with them](autoscaling-vs-reserved-instances.md)
- [Reserved, Scheduled and Spot instances as AWS cost levers](aws-instance-purchasing-models-cost.md)
- [Estimating small WVD environments in the Azure calculator](azure-calculator-small-wvd-trick.md)
- [Azure cost-control habits for a test lab](azure-classic-cost-control-takeaways.md)
- [Azure cost levers: CSP, right-sizing, promos and Reserved Instances](azure-cost-levers-csp-vm-sizing-ri.md)
- [Azure Ephemeral OS disks for stateless WVD workloads](azure-ephemeral-os-disks.md)
- [Azure On-demand Capacity Reservation Cheat Sheet](azure-on-demand-capacity-reservation-cheat-sheet.md)
- [Cloud cost-optimization levers](cloud-cost-optimization-levers.md)
- [Indicative cost overview: split the totals, show the assumptions, never call it a quote](indicative-cost-overview-method-assumptions-and-reserved-instances.md)
- [Reserved Instances: 12% early-exit fine and monthly payment](reserved-instance-early-exit-fine.md)
- [The Azure calculator is fine, but MSPs need a real one](use-vendor-calculators-not-just-azure.md)
- [Estimating WVD cost for under-100-user environments with the Azure calculator](wvd-azure-calculator-small-environment-method.md)
- [WVD session hosts are charged at Linux compute rates](wvd-charged-at-linux-rates.md)
