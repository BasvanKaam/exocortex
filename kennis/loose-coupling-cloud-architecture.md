---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-10
tags: [cloud, architecture, loose-coupling, resiliency]
layer: reference
gedateerd: nee
bron: basvankaam-blog
---

# Loose coupling as a core Cloud design principle

Featured in the project as a contributed design-principle example (by Rajeev Kumar): IT systems should be designed to reduce inter-dependencies. Components should be loosely coupled so a change or failure in one does not affect others, interacting only through well-defined, technology-agnostic interfaces. Service discovery lets smaller services be consumed without prior knowledge of network topology. Asynchronous integration via an intermediate durable storage layer (e.g. a queue) decouples a producer from a consumer and adds resiliency: if the reader fails, messages still queue for later processing. Designing applications to handle component failure gracefully reduces end-user impact.

Durable cloud-native architecture thinking; not Bas's own words but curated and endorsed by him in the project.

*Bron: blogpost 'Byte sized Cloud design principles and architectural recommendations' (2019-01-30), basvankaam.com.*

## Verwante notities

- [Bas leans into hyper-convergence and web-scale as the future](bas-on-web-scale-as-future-of-it.md)
- [Byte-Sized: Cloud Design Principles and Architectural Recommendations book](byte-sized-cloud-design-book.md)
- [Cloud is about far more than technology](cloud-is-more-than-technology.md)
- [Cloud-Native: Designed for the Cloud from the Start](cloud-native-definition.md)
- [FaaS / Serverless Computing Explained](faas-serverless-explained.md)
- [Converged (hyperconverged) infrastructure collapses compute and storage into one appliance](nutanix-converged-infrastructure-concept.md)
- [Post-COVID resilience: BCPs, redundancy, supply chains, automation](post-covid-resilience-measures.md)
- [SCAF Design Principles and Why It Exists](scaf-design-principles.md)
- [Virtualization is a part of cloud, not the same thing](virtualization-is-not-cloud.md)
- [Web-scale architecture: software-defined, scale-out, self-healing on x86](web-scale-architecture-principles.md)
