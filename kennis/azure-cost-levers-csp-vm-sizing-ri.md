---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-11
tags: [azure, cost-optimization, csp, reserved-instances, vm-sizing]
layer: reference
gedateerd: ja
bron: nerdio-blog
---

# Azure cost levers: CSP, right-sizing, promos and Reserved Instances

Bas's practical checklist for getting Azure spend down. Two flavours of saving: items that cut the list price directly, and items that just make resources run more efficiently (so you spend less without changing the per-unit price).

CSP program (public Microsoft program): becoming a CSP makes it easier to transact Azure (create customer subscriptions) and gives a discount off Azure list price via the CSP Provider, plus incentives tied to Microsoft growth objectives that can add up to ~10% or more. Two types: Direct CSP (buy directly from Microsoft, must maintain high consumption volume and clear qualification hurdles) and CSP Reseller (buy through an Indirect CSP Provider/distributor, no volume commitment or certification hurdle, so any MSP can become one). Indicative public discount bands he cites (his caveat: these change over time, no guarantee): Azure consumption 7-15%, Reserved Instances 1-5%, CSP Software Subscriptions 5-15%, Office 365 / Dynamics 365 / Microsoft 365 10-20%, plus regional accelerators/rebates that vary.

Right-size the VM, do not copy on-prem specs: on-prem physical/virtual machines are often oversized. In the cloud you can start small (even too small) and resize within minutes, so do not pay for reserved capacity you will not need in year one. Azure Migrate (supports Hyper-V and VMware) can recommend the correct VM size based on stats.

Promos: Microsoft periodically discounts VM families. Example he cites (dated): a 30% discount on D-series and Bs-series Windows VMs used in a WVD host pool, Jan 5 - Mar 31 2021 offer window, discount applied for 90 days after redemption, then standard rates resume. Watch for current equivalents rather than reusing the dates.

Reserved Instances: a list-price lever for steady-state, always-on workloads.

*Bron: Nerdio-content 'How to save money on the Microsoft Azure list price' (Blogs).*

## Verwante notities

- [Azure Hybrid Benefit and the Linux-Pricing 'Fun Fact'](azure-hybrid-benefit-explainer.md)
- [Azure Reserved Instances: How They Work and When to Use Them](azure-reserved-instances-explainer.md)
- [How Azure Reserved Instances and Hybrid Benefit work](azure-ri-ahb-mechanics.md)
- [B-series burstable VMs: the CPU-credit model and when to use them](b-series-burstable-vms-explained.md)
- [Choosing a CSP: Azure as the Default for Microsoft Shops](csp-platform-choice-azure-default.md)
- [Ephemeral OS disks: free, fast, stateless, and the deallocate caveat](ephemeral-os-disks-explained.md)
- [Nerdio Cost-Optimization Levers (Bas's Assessment Method)](nerdio-cost-optimization-levers.md)
- [Bas on sizing: there is no 'one size fits all', and don't overdo it](sizing-no-one-size-fits-all.md)
- [Size virtual desktops by testing, not by general guidelines](wvd-sizing-test-dont-trust-guidelines.md)
