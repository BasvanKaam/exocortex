---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-10
tags: [WVD, Azure, pricing, AHU, reserved-instances]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Estimating small WVD environments in the Azure calculator

How it worked in mid-2020. When you select Windows Virtual Desktop in the Azure pricing calculator it defaults to 100 users (the minimum) and snaps back to 100 if you enter fewer, unless you work with the peak/off-peak concurrency fields.

Workaround for a smaller estimate (dozens of users): instead of adding WVD directly, calculate individual supported VMs (e.g. a D8s v3, 8 vCPU / 32 GB, plus a Premium SSD), then toggle Azure Hybrid Benefit and a 1- or 3-year reservation and watch the price drop. Because WVD VMs already have AHU applied automatically, a manual single-VM calc with AHU on lands at the same price as adding WVD, while letting you size for a handful of users (one D8s v3 serves roughly 15-20 users at normal-to-heavy usage).

Microsoft assumes you hold proper Windows licenses when you pick WVD, so the calculator gives no option to include/exclude the Windows license: the AHU discount is baked in.

*Bron: blogpost 'How to: Calculating costs for smaller WVD environments using the Azure Calculator' (2020-06-24), basvankaam.com.*

## Verwante notities

- [M365 E3 already entitles you to AHU for WVD](ahu-entitlement-via-m365-e3.md)
- [Autoscaling can beat Reserved Instances, and pairs with them](autoscaling-vs-reserved-instances.md)
- [How Azure Reserved Instances and Hybrid Benefit work](azure-ri-ahb-mechanics.md)
- [The Azure calculator is fine, but MSPs need a real one](use-vendor-calculators-not-just-azure.md)
- [WVD session hosts are charged at Linux compute rates](wvd-charged-at-linux-rates.md)
