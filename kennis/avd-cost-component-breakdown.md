---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [avd, azure, kosten, fslogix, compute, dated]
layer: reference
gedateerd: ja
bron: nerdio-blog
---

# AVD cost-component breakdown

Based on analysis of several thousand Nerdio-managed AVD deployments (5 to 10,000+ users), the monthly cost of a typical AVD environment falls into five buckets:

- Compute (session-host VMs): ~70%
- OS disk storage (managed disks on session hosts): ~12%
- FSLogix storage (Azure Files / Azure NetApp Files for profiles): ~9%
- Networking (egress, VPN gateways, global VNet peering): ~3%
- Other (images, Log Analytics, Azure Automation, backup): ~6%

The first three make up more than 90% of total cost, so any serious cost-reduction effort targets compute, OS disks and FSLogix profile storage first. Optimizing images and the rest yields only marginal savings.

Use this as the prioritization frame before any AVD cost exercise: compute is by far the largest lever, profile and OS-disk storage are the secondary levers.

*Bron: Nerdio-content 'Significantly lowering your costs for Azure Virtual Desktop using these 5 cost reduction options' (Blogs).*

## Verwante notities

- [The Real Blocker to AVD Adoption Is the Cost Conversation](avd-adoption-is-blocked-by-the-cost-conversation.md)
- [AVD Cost Modelling: Modeler + User Cost Attribution](avd-cost-modelling-modeler-and-cost-attribution.md)
- [Five (plus RI) AVD cost-reduction options](avd-five-cost-reduction-options.md)
- [Framing a native-vs-Nerdio WVD business case](native-vs-nerdio-wvd-business-case-framework.md)
- [Nerdio Cost-Optimization Levers (Bas's Assessment Method)](nerdio-cost-optimization-levers.md)
- [Nerdio non-technical cost levers](nerdio-non-technical-cost-levers.md)
- [Settings for Success: Nerdio cost-optimization checklist](nerdio-settings-for-success-cost-checklist.md)
- [Nerdio Manager for WVD: the cost-saving levers (WVD era)](nmw-cost-saving-levers-overview.md)
