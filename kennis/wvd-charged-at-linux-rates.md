---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-10
tags: [WVD, Azure, pricing, AHB, Linux]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# WVD session hosts are charged at Linux compute rates

Microsoft (2020): Windows Virtual Desktop session host VMs are charged at Linux compute rates for Windows 10 single-session, Windows 10 multi-session and Windows Server. In the Azure calculator, turning on Azure Hybrid Benefit on a Windows VM yields the same price as selecting a Linux license, but only for the default CentOS, or Ubuntu, or SUSE Linux Enterprise; other Linux versions cost more.

Bas's caveat: do not use Linux pricing as a proxy for AHB when calculating, because AHB specifically means bringing an existing owned Windows/SQL license (with SA) into Azure, and not all Linux licenses are priced equally.

*Bron: blogpost 'What you need to know about Azure Reserved Instances, AHB and WVD' (2020-07-07), basvankaam.com.*

## Verwante notities

- [M365 E3 already entitles you to AHU for WVD](ahu-entitlement-via-m365-e3.md)
- [Autoscaling can beat Reserved Instances, and pairs with them](autoscaling-vs-reserved-instances.md)
- [Estimating small WVD environments in the Azure calculator](azure-calculator-small-wvd-trick.md)
- [How Azure Reserved Instances and Hybrid Benefit work](azure-ri-ahb-mechanics.md)
- [Reserved Instances: 12% early-exit fine and monthly payment](reserved-instance-early-exit-fine.md)
- [The Azure calculator is fine, but MSPs need a real one](use-vendor-calculators-not-just-azure.md)
- [WVD introduced multi-user Windows 10 and a license-based entitlement model](wvd-win10-multiuser-and-licensing.md)
