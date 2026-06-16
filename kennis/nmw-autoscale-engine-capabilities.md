---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [nerdio, nmw, autoscale, wvd, avd, host-pool]
layer: reference
gedateerd: ja
bron: nerdio-blog
---

# What the Nerdio autoscale engine does (NMW era)

Bas's plain-English explainer of the autoscale engine in Nerdio Manager for WVD. Dated: reflects the Nerdio Manager for WVD (NMW) product naming and feature state at time of writing.

For a **dynamic hostpool**, the autoscale engine manages the machines for you, fully automated:
- Start, stop, reboot machines.
- Build new VMs from scratch and add them; completely remove machines when no longer needed.
- Monitor hosts and repair/heal them when needed.
- Put machines in **drain mode** when applicable.
- Notify users that something is about to happen, using your own message text.
- Give each machine a unique hostname (which it can reuse) and manage the underlying computer objects in Active Directory.

Works across hosted shared environments, published applications, non-persistent pooled desktops, and personal assigned persistent desktops.

**Static vs dynamic hostpool:** static means you add/remove/start/stop VMs manually and bring your own monitoring; dynamic hands all of that to the autoscale engine. Bas cites average savings on underlying compute and storage of up to 75% with dynamic hostpools.

**Self-service angle:** users can be allowed to start/stop/restart their own personal assigned VMs and log off their own sessions, giving them more flexibility/responsibility.

## Related
- nmw-install-from-azure-marketplace
- common-wvd-adoption-challenges

*Bron: Nerdio-content 'How to deploy a complete WVD environment for your office in minutes instead of days or weeks' (Blogs).*

## Verwante notities

- [How Nerdio's WVD autoscale worked: triggers, base/burst capacity, graceful drain](nerdio-autoscale-mechanics-2020.md)
- [Nerdio autoscaling engine: pooled hostpool scaling logic](nerdio-autoscaling-engine-pooled-hostpools.md)
- [Nerdio autoscaling for personal/persistent desktops](nerdio-autoscaling-personal-persistent-desktops.md)
- [Static vs dynamic host pools in Nerdio (autoscale eligibility)](nerdio-static-vs-dynamic-host-pools.md)
- [Nerdio Manager for WVD core capabilities circa 2020](nmw-core-capabilities-2020.md)
- [Nerdio Manager for WVD: the cost-saving levers (WVD era)](nmw-cost-saving-levers-overview.md)
- [Hybrid WVD Object Model (NMW, Fall/Spring era)](nmw-hybrid-wvd-object-model.md)
- [Installing Nerdio Manager for WVD from the Azure Marketplace](nmw-install-from-azure-marketplace.md)
- [The NMW thesis: automation and hiding complexity](nmw-thesis-automation-hiding-complexity.md)
- [Static vs dynamic host pools and autoscaling (Nerdio)](static-vs-dynamic-hostpools-nerdio.md)
