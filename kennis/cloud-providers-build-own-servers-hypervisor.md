---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-09
tags: [azure, microsoft, hypervisor, hyper-v, datacenter, availability-zone]
layer: reference
bron: van-de-basis-tot-meester-in-de-cloud
---

# Cloud providers build their own servers and hypervisors

Microsoft (and the other large Cloud providers) design and build their own servers and hypervisor technology to save costs and optimise the performance of their Azure datacenters, giving full control over hardware and software. Microsoft's datacenters - also called Availability Zones - form the backbone of Azure and use custom server designs optimised for Cloud computing, letting Microsoft manage the infrastructure lifecycle from design to rollout.

Microsoft also developed its own hypervisor, a lighter optimised version built on Hyper-V. The Azure hypervisor offers improved isolation and security for VMs, with a notable integrated hypervisor-firewall that filters unwanted traffic without needing separate external hardware firewalls, lowering complexity and cost. This approach reduces dependence on external hardware suppliers (to a degree) and lets Microsoft innovate faster.

Capacity is not always unlimited, though: shortages can occur in certain Azure regions, e.g. when not enough GPU VMs are available (Microsoft uses NVIDIA and AMD GPUs). They eventually resolve it, but it can take a while.

## Verwante notities

- [The Azure cloud hierarchy: tenant down to resources](azure-cloud-hierarchy.md)
- [Azure high-availability building blocks](azure-high-availability-building-blocks.md)
- [Microsoft Azure Profile and Strengths](azure-profile-strengths.md)
- [Hyperscaler security investments and certifications](cloud-provider-security-investments.md)
- [Core cloud building blocks: datacenter, virtualization, APIs, storage, databases, elasticity](core-cloud-components-and-concepts.md)
- [The less-obvious challenges of building datacenters](datacenter-hidden-challenges.md)
- [Global cloud scale: regions, zones, and which continent has no datacenters](global-scale-regions-zones-datacenters.md)
- [Bas: look critically at 'green' datacenter claims](green-cloud-claims-critical-look.md)
- [Microsoft sustainability goal: carbon negative by 2030](microsoft-carbon-negative-2030.md)
- [Bas on the physical scale: subsea cables and an Azure datacenter tour](submarine-cables-and-datacenter-scale.md)
