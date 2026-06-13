---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [azure, gpu, nvv4, avd, wvd, cost-optimization]
layer: reference
gedateerd: ja
bron: nerdio-blog
---

# Azure GPU VMs: NVIDIA vs AMD NVv4, licensing and partitioning

GPU-enabled VMs are not only for graphics-heavy workloads. The whole Office/Microsoft 365 suite, Windows 10, and browsers all benefit from a GPU. A GPU is not always required, but worth researching before deciding.

## What holds companies back: cost and licensing
- The biggest barrier is cost, and how GPUs are licensed (especially NVIDIA) plays a large part.
- **NVIDIA** is more flexible/advanced on performance but more expensive. On-prem you buy a physical NVIDIA GPU **plus** a separate virtual GPU software license matched to your use case (Virtual Applications, Virtual PC, Virtual Datacenter Workstation, Virtual Compute Server).
- The vGPU software is licensed separately from the physical card: either an **annual subscription** or **perpetual** license, both priced per user. Perpetual additionally needs a SUMS license (Support, Updates, Maintenance and Subscription) at yearly cost; that is bundled in the annual license. SUMS gives access to new software releases plus technical support.
- On Azure these costs are folded into the overall package.

## AMD NVv4 (the differentiator)
- NVv4 VMs are powered by AMD Radeon Instinct MI25 GPUs with AMD EPYC "Rome" CPUs.
- USP: the MI25 can be **partitioned** into smaller GPU segments assigned to individual VMs, from 1/8th of a GPU (2 GiB frame buffer) up to a full GPU (16 GiB frame buffer).
- You just buy the physical GPU, no separate vGPU software license layer like NVIDIA.
- NVv4 supports up to 32 vCPUs, 112 GB RAM, 16 GB GPU memory.
- NVIDIA-backed Azure GPU VMs (N-series) as of writing **cannot** be partitioned/spread across multiple VMs.

## Practical guidance
Pick the VM that fits your use case and budget. Do not judge on price alone, test, because it is cloud and that is easy. Combine GPU partitioning with autoscaling, Ephemeral OS disks, reserved instances and Azure Hybrid Benefit to drive total cost down.

*Bron: Nerdio-content 'How to get the most out of your GPU enabled machines at the lowest cost possible, including a deeper dive into the Nerdio autoscaling engine' (Blogs).*

## Verwante notities

- [Azure Hybrid Benefit and the Linux-Pricing 'Fun Fact'](azure-hybrid-benefit-explainer.md)
- [Ephemeral OS Disks for AVD: free, fast OS storage for stateless hosts](ephemeral-os-disks-for-avd.md)
- [GPUs in VDI: a tool in the toolbox, not a default](gpu-in-vdi-tool-in-the-toolbox.md)
- [Nerdio autoscaling engine: pooled hostpool scaling logic](nerdio-autoscaling-engine-pooled-hostpools.md)
- [Test GPU VMs, don't decide on price alone](test-dont-trust-pricing-on-gpu-vms.md)
