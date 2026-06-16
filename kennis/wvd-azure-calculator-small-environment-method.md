---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [wvd, azure, cost, calculator, ahb, reserved-instances, method]
layer: reference
gedateerd: ja
bron: nerdio-blog
---

# Estimating WVD cost for under-100-user environments with the Azure calculator

Bas's workaround for a real limitation: the Azure pricing calculator's WVD line item forces a 100-user minimum (change it to 50 and it snaps back to 100), so you can't directly price a small deployment. WVD-era; verify current calculator behavior before relying on the exact steps.

## The trick
Price a single VM line item instead of the WVD line item, then divide.
1. Pick a supported WVD VM (his example: D8s v3, 8 vCPU, 32 GB).
2. Add a Premium SSD (e.g. 256 GB).
3. Apply Azure Hybrid Benefit, then apply 3-year reserved, and watch the price drop.
4. Cross-check: add the WVD line item with the same VM/SSD config; for a heavy workload Microsoft assumes ~2 users per vCPU, so 100 users needs ~6 machines. Five extra single-VM lines match the WVD price, proving AHB is already baked into the WVD line item.
5. One such VM serves roughly 15-20 users at normal-to-heavy usage; scale by using bigger machines or (preferably) multiple smaller ones. Same logic for GPU machines, usually only a handful of users.

## Cost levers it leans on
- Azure Hybrid Benefit (AHB): the WVD calculator silently applies it because Microsoft assumes you hold proper licenses when you select WVD; you get no checkbox to toggle it.
- Reserved instances: can now be paid monthly (opex, not capex up front). Early exit costs a 12% fee on the remaining unused term, so a 1- or 3-year reservation is essentially always cheaper than pay-as-you-go.

## Licensing that entitles WVD + AHB
M365 E3 (and E5/A3/A5/F3/Business Premium) pre-pays for both Windows 10 Enterprise multi-session and single-session, so AHB applies. Windows E3/E5/A3/A5 also qualify. Other AHB routes: Windows Server via EA/volume licensing with active Software Assurance (rare for MSPs), or Windows Server via CSP Software Subscriptions (more relevant for MSPs; SQL Server and RDS available the same way). SQL Standard licensed per core under SPLA can be paid monthly and includes AHB.

Naming note: as of 21 April 2020 the O365 SMB SKUs were renamed to Microsoft 365.

*Bron: Nerdio-content 'How to Calculating costs for smaller WVD environments using the Azure Calculator' (Blogs).*

## Verwante notities

- [M365 E3 already entitles you to AHU for WVD](ahu-entitlement-via-m365-e3.md)
- [Estimating small WVD environments in the Azure calculator](azure-calculator-small-wvd-trick.md)
- [Azure Hybrid Benefit and the Linux-Pricing 'Fun Fact'](azure-hybrid-benefit-explainer.md)
- [Azure Reserved Instances: How They Work and When to Use Them](azure-reserved-instances-explainer.md)
- [How Azure Reserved Instances and Hybrid Benefit work](azure-ri-ahb-mechanics.md)
- [For steady WVD workloads, reserved instances almost always win](reserved-instances-almost-always-cheaper-position.md)
- [Size virtual desktops by testing, not by general guidelines](wvd-sizing-test-dont-trust-guidelines.md)
