---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-10
tags: [web-scale, converged-infrastructure, software-defined, scale-out, nutanix]
layer: reference
gedateerd: nee
bron: basvankaam-blog
---

# Web-scale architecture: software-defined, scale-out, self-healing on x86

Web-scale (a.k.a. converged) architecture, as the hyperscalers (Google, Amazon, Facebook) pioneered and Bas explained it:

- Software-defined: intelligence is in software, making it flexible, fault tolerant, scalable and able to run on standard x86 / commodity hardware (Google famously builds its own white-label hardware to keep costs low).
- Converged: compute, storage, networking and virtualization combined into a single platform/appliance; resources are aggregated and pooled. Storage (often flash/SSD) and partly-virtualized networking sit local to the VMs, boosting performance.
- Scale-out, not scale-up: add nodes when you need them ('scaling on demand'), avoiding over-provisioning; workloads scale without scaling up individual servers.
- Centralized, simple management: managed as a single entity no matter the size; a basic infra should stand up in 30-45 minutes 'if not, it's simply no good.'
- Self-healing: the software acts on failures by moving workloads to a healthy, least-loaded node while faulty hardware is replaced non-disruptively. Underpinned by dedup, data tiering, replicated writes and redundant components.

These are durable principles that became mainstream hyperconverged / cloud-native infrastructure thinking.

*Bron: blogpost 'What is Web-Scale technology and where does it come from?' (2014-06-18), basvankaam.com.*

## Verwante notities

- [Bas leans into hyper-convergence and web-scale as the future](bas-on-web-scale-as-future-of-it.md)
- [Web-scale will make today's best practices obsolete, change is coming fast](best-practices-will-become-just-practices.md)
- [What a converged infrastructure is](converged-infrastructure-definition.md)
- [Converged infrastructure will displace SAN-centric design](converged-will-displace-san-centric-design.md)
- [HP Moonshot is converged but not truly web-scale](hp-moonshot-is-not-web-scale.md)
- [Loose coupling as a core Cloud design principle](loose-coupling-cloud-architecture.md)
- [Converged (hyperconverged) infrastructure collapses compute and storage into one appliance](nutanix-converged-infrastructure-concept.md)
- [Virtualization is a part of cloud, not the same thing](virtualization-is-not-cloud.md)
- [OEM deals will democratize web-scale infrastructure](web-scale-for-everyone-prediction.md)
