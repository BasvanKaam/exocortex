---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [nerdio, avd, cost-optimization, autoscale, method]
layer: reference
gedateerd: ja
bron: nerdio-content
---

# Nerdio Cost-Optimization Levers (Bas's Assessment Method)

Bas's reusable way of walking an estate through where the money actually leaks, beyond the headline autoscale story. The levers, in the order he reaches for them:

- **Swap attached disks on shutdown.** Each VM carries a disk. Premium SSD during business hours for a good experience; when the machine is de-allocated, Premium is wasted. Nerdio autoscale can swap the attached disk to a cheaper tier (e.g. Standard HDD, ~70% cheaper) while the machine is down. Storage is cheap per machine, but across hundreds or thousands of machines it adds up to real savings.
- **Turn Azure Files into pay-per-use.** Premium tier ships with 100GB by default. Nerdio's storage scaling engine auto-grows and auto-shrinks file shares in fixed GB increments or by percentage, so you stop pre-provisioning (and paying for) allocated-but-unused capacity. The same principle applies, with a few exceptions, to Azure NetApp Files.
- **Clean up stale FSLogix profiles.** Azure Files commonly back FSLogix profile containers. Scripted actions can periodically scan profiles and remove the ones no longer in use, freeing storage and lowering cost.
- **Optimize the Log Analytics Workspace.** A LAW always sits alongside AVD for monitoring samples. It can be tuned/optimized in Nerdio; savings scale with deployment size and on larger estates run into the thousands per month.
- **Right-size the SKU.** Look at the SKUs in use and their utilization. Over-utilized SKUs justify a heavier machine; under-utilized ones justify a cheaper SKU. Nerdio's recommendation engine proposes alternative VM types from historical data while holding performance steady. The lever works even on reserved cores because it lowers the quantity/size reserved.
- **Prefer multi-user over single-user where the persona allows.** Multi-user machines share CPU/GPU/RAM and installed apps across users, which is the economical default for most workloads. They are heavier per box, but the total core count (the thing that gets reserved) drops, so it is cheaper overall. Mix single- and multi-user by persona and application type.

Headline figure Bas uses: layering autoscale on top of reserved/on-demand reserved capacity gets an additional ~25-30% savings versus RIs/reserved capacity alone, often more.

See also: reserved-instances-do-not-guarantee-compute, nerdio-active-active-dr.

*Bron: Nerdio-content 'MCS' ((root)).*

## Verwante notities

- [Auto-scale first, then reserve the residual](auto-scale-before-reserved-instances.md)
- [AVD cost-component breakdown](avd-cost-component-breakdown.md)
- [AVD Cost Modelling: Modeler + User Cost Attribution](avd-cost-modelling-modeler-and-cost-attribution.md)
- [Five (plus RI) AVD cost-reduction options](avd-five-cost-reduction-options.md)
- [AVD / Windows 365 Discovery Questions (Bas's Talking Points)](avd-w365-discovery-questions.md)
- [Azure cost levers: CSP, right-sizing, promos and Reserved Instances](azure-cost-levers-csp-vm-sizing-ri.md)
- [Azure Hybrid Benefit and the Linux-Pricing 'Fun Fact'](azure-hybrid-benefit-explainer.md)
- [The 7 Cloud Baby Steps (behavior-driven FinOps)](cloud-baby-steps-behavior-driven-finops.md)
- [A license is free if it returns more than it costs](licenses-that-make-you-money.md)
- [Active/Active DR for AVD Across Two Regions](nerdio-active-active-dr.md)
- [Nerdio Manager storage autoscale for Azure Files Premium](nerdio-azure-files-premium-autoscale.md)
- [Nerdio non-technical cost levers](nerdio-non-technical-cost-levers.md)
- [NME first-admin RBAC and log analytics retention savings](nme-rbac-first-admin-and-savings.md)
- [Nerdio Manager for WVD: the cost-saving levers (WVD era)](nmw-cost-saving-levers-overview.md)
- [Shutting Down Reserved Machines Saves Nothing on Compute](position-shutting-down-reserved-machines-saves-nothing.md)
- [The True ROI Is Time and Wellbeing, Not Just Money](position-true-nerdio-roi-is-time-and-wellbeing.md)
- [Reserved Instances Do Not Guarantee Compute Availability](reserved-instances-do-not-guarantee-compute.md)
