---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-11
tags: [migration, modernization, workload, scaf, decision, method]
layer: reference
gedateerd: nee
bron: salomon-masterclass
---

# Migrate vs Modernize as a Per-Workload Decision

In the SCAF teaching, Bas insists on making an explicit per-workload distinction between **migration** (move the workload more or less as-is) and **innovation / modernization** (re-shape the workload for cloud). The decision is made at the level of the individual workload, not the whole estate, and it shapes which target services you reach for.

He frames a workload as a collection of IT assets (servers, VMs, applications, data, appliances) that together support a defined process; a workload can support more than one process and can depend on shared assets or larger platforms, but it should have defined boundaries around its dependencies. Workloads can often be made visible by monitoring network traffic between assets.

Worked examples he uses to make the distinction concrete:
- Acquisition -> rationalize existing systems (migration).
- A virtual design platform -> innovation.
- A new HR system -> look at the underlying web servers and databases (e.g. PaaS), cloud vs on-prem.
- Improving the online user experience of an existing service -> web servers, databases, line connections, serverless.
- An automated helpdesk bot for support -> faster search and processing of data.
- Place-independent productivity for field staff (construction sites, planes, trucks, police).
- Experimenting with Big Data, VR, IoT (new).

*Bron: Salomon-IT 'SCAF - Aantekeningen'.*

## Verwante notities

- [Commodity vs competitive applications as the core strategy lens](commodity-vs-competitive-application-lens.md)
- [Criteria for Selecting the First Workload to Migrate](first-workload-selection-criteria.md)
- [Migration strategy framework: transition vs transformation, big-bang vs phased, build-clean-alongside](migration-strategy-decision-framework.md)
- [Definitive Cloud and Refactor Choice (Rationalisation)](rationalisation-refactor-choice-execution.md)
- [SCAF: Application, Data and System Inventory via Waves](scaf-application-data-system-inventory.md)
- [SCAF implementation/migration planning template structure](scaf-implementation-migration-template.md)
- [Tactical Cloud Migration Prioritization](tactical-cloud-migration-prioritization.md)
