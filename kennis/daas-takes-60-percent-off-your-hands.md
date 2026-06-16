---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [daas, avd, shared-responsibility, broker, infrastructure, rule-of-thumb]
layer: rich
bron: van-de-basis-tot-meester-in-de-cloud
---

# DaaS Takes Roughly 60% Off Your Hands

A Bas rule of thumb: the big difference between DaaS and self-managed VDI lies mainly in which components you do or don't have to maintain. On paper, taking single-/multi-session systems from the cloud may cost more — but whether it actually does is questionable.

The components DaaS removes from your responsibility: the underlying physical machines (on which the VMs run), power, cooling, network, storage, and the various roles needed — load balancing of sessions, the broker layer that handles access, web server, database, and so on. Bas estimates roughly **60 percent** of the work and responsibilities are taken off your hands, depending on the use case (what the machines are used for). Single or multi-user makes little difference here.

His dishwashing analogy for the 'As a Service' principle: "Je gaat, als je net uit eten bent geweest, ook niet zelf de afwas doen, toch?" (After you've just been out to dinner, you don't go and do the dishes yourself, do you?) — if you take something As a Service, it's taken care of for you.

Nuance he raises himself: you can question whether AVD even counts as DaaS, since you still manage parts of the infrastructure yourself (network, storage, scaling VMs up/down) — assuming your organisation sets up, configures and maintains AVD itself. It depends on who bears which responsibility and who pays whom; e.g. an internal IT department offering AVD as a service can be seen as the provider (DaaS supplier), with user groups/cost centers as the unburdened customers.

## Bron-citaten (NL, verbatim)

> “Je gaat, als je net uit eten bent geweest, ook niet zelf de afwas doen, toch?”

## Verwante notities

- [AVD - The Only Cloud Service That Runs Windows Client Multi-User](avd-windows-client-multi-user.md)
- [DaaS / VDI Additions to the Technical Design](daas-vdi-technical-design-considerations.md)
- [DaaS provider takes roughly 60% of the management off the IT department](daas-vendor-takes-60-percent-of-management.md)
- [DaaS versus VDI](daas-vs-vdi.md)
- [Bas's reframe: is AVD and/or Windows 365 Cloud PC really DaaS?](is-avd-and-windows-365-really-daas.md)
- [Transformation: From Product to Service, Ownership to Usage](product-to-service-ownership-to-usage.md)
- [Shared Responsibility Model (Restaurant Analogy)](shared-responsibility-model-restaurant-analogy.md)
