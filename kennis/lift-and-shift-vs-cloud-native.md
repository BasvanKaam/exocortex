---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-11
tags: [cloud, lift-and-shift, cloud-native, serverless, iac, paas, migration-strategy]
layer: reference
gedateerd: nee
bron: salomon-it-blog
---

# Lift-and-shift vs cloud-native: where cloud value actually lives

Bas distinguishes two fundamentally different ways of using cloud, and argues most of the value sits in the second.

**Lift-and-shift (rebuilding what you have).** You take what already runs in your own datacenter (VMs, databases, Linux webservers, directory services, fileservers, network components, remote access, proxies, hundreds of often in-house, complex line-of-business apps) and rebuild it in a cloud. It is easy and fast, much of it automated. But you end up with a pile of maintenance-heavy virtual machines. The verdict: effective yes, efficient no. You gain flexibility (easy scale up/down, minimal upfront investment) but your maintenance burden and day-to-day operations barely change, and you usually do not save money.

**Cloud-native (a different way of thinking).** The real power of cloud shows when you use Serverless, Platform as a Service (PaaS), Infrastructure as Code, REST APIs, microservices and containers. Most of your infrastructure disappears: no (or minimal) VMs, fileshares, traditional storage, installs, patching. It is still there, you just see and notice little of it. This costs time and money up front (so the "no upfront investment" promise no longer holds short term), but on the medium-to-long term real savings are very realistic, pay-for-what-you-use becomes genuinely interesting, time-to-market improves and error rates drop.

**The catch.** Cloud-native requires redesigning, rebuilding and sometimes rewriting existing systems and apps (not always possible). Lack of in-house expertise is stumbling block number one. The cloud services themselves are still maturing and miss certain functionality (varies per provider). Not every environment lends itself to it, fully or partially.

Reference examples he cites: A Cloud Guru (training platform fully built on Serverless and IaC) and Netflix (microservice architectures, Serverless, PaaS). Size does not decide; the size of the required upfront investment is what you must think hard about.

*Bron: blogpost 'CLOUD, als je doet wat je altijd al deed' (2019-04-02), salomon-it.nl.*

## Verwante notities

- [Cloud is not a different way of working, it demands a different way of thinking](cloud-demands-different-thinking-not-different-working.md)
