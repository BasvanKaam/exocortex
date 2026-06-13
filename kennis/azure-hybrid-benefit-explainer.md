---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [azure, hybrid-benefit, licensing, cost-optimization, wvd]
layer: reference
gedateerd: ja
bron: nerdio-blog
---

# Azure Hybrid Benefit and the Linux-Pricing 'Fun Fact'

Azure Hybrid Benefit (AHB) lets you bring an existing Windows Server and/or SQL license (already owned with Software Assurance, or via a CSP subscription) into Azure so you don't pay for the OS/SQL license on Azure compute. Often a major discount, and frequently combined with Reserved Instances.

Licensing constraints to remember:
- Windows Server Standard: licenses transfer to a cloud VM and can no longer be used on-prem. Up to two VMs in Azure (max 16 cores).
- Windows Server Datacenter: up to two VMs in Azure AND any number on-prem (e.g. on Hyper-V).

Bas's 'fun fact' / nuance: turning on AHB in the Azure Calculator gives the same VM price as selecting a Linux license, but only at default CentOS, or Ubuntu, or SUSE Linux Enterprise; all other Linux versions are more expensive. Microsoft says WVD session-host VMs (Win10 single, Win10 multi-session, Windows Server) are charged at Linux compute rates, but Bas's point is that this isn't entirely correct since it depends on the Linux version selected. He recommends NOT using Linux pricing as a stand-in for AHB when comparing in the calculator; treat it as trivia, not a method.

*Bron: Nerdio-content 'What you need to know about Azure Reserved Instances, Azure Hybrid Benefit and WVD' (Blogs).*

## Verwante notities

- [Autoscaling Can Beat Reserved Instances for Variable WVD Workloads](autoscaling-vs-reserved-instances-stance.md)
- [Azure cost levers: CSP, right-sizing, promos and Reserved Instances](azure-cost-levers-csp-vm-sizing-ri.md)
- [Azure GPU VMs: NVIDIA vs AMD NVv4, licensing and partitioning](azure-gpu-vms-licensing-and-nvv4-partitioning.md)
- [Azure Reserved Instances: How They Work and When to Use Them](azure-reserved-instances-explainer.md)
- [B-series burstable VMs: the CPU-credit model and when to use them](b-series-burstable-vms-explained.md)
- [Nerdio Cost-Optimization Levers (Bas's Assessment Method)](nerdio-cost-optimization-levers.md)
- [For steady WVD workloads, reserved instances almost always win](reserved-instances-almost-always-cheaper-position.md)
- [Estimating WVD cost for under-100-user environments with the Azure calculator](wvd-azure-calculator-small-environment-method.md)
