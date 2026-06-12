---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-11
tags: [inventarisatie, assessment, intake, rationalisatie, business-case, cloud-migratie]
layer: reference
gedateerd: nee
bron: salomon-opdrachten
---

# Cloud inventory method: joint assessment, waves, and the R's

How I run the assessment that underpins a defensible cloud migration proposal. An accurate inventory of applications, backend systems and data including all dependencies is the precondition for saying anything credible about what moves where and in what form.

## Do it together, in waves
- Inventory **jointly** with the client. Two pairs of eyes see more than one: while one dictates, the other notes, and you get a first feel for options on the spot and document where possible.
- An outsider glancing at the landscape can't say anything useful about dependencies or volumes, so the client's own knowledge is gold and goes in early.
- Work in **waves**. A single pass rarely gives the full picture. Each wave refines the cut: high / medium / low priority and impact, cloud or not, and in which form. Always capture quantities and counts (storage, backup units, switches, routers, firewalls, network links count as "systems" too).
- A focused inventory like this is realistically a 3-to-4-day effort given the time and access.

## The R's decide the "how"
The "how to cloud" takes different forms per workload: Retire, Rehost, Refactor, and the rest of the R's. This rationalization choice is sketched in the Insight pillar and made final in Execution. Tooling that supports management or other processes is part of the inventory too.

## Scale reference
A mid-size landscape in this kind of engagement was roughly 40 systems and 125-150 applications. Useful as a yardstick for effort.

## Dependency / characteristic checklist (test every component against this)
- Latency sensitivity and other network requirements
- Where the data lives in the new (cloud) situation; data classification (is it allowed in the cloud)
- Large data volumes involved?
- Dependency on OS, system, dongle or other hardware
- Dependency on other applications (database or otherwise)
- Certified/suitable for multi-user use?
- Specific security requirements: encryption, authentication
- Minimum / desired system requirements
- I/O dependencies
- Install type: installed (part of image), virtualized (how), other
- Is it a core-business app, and what is the impact/priority if it is unavailable

Where no detail is available, a simple yes/no per item is enough to move forward.

## Business case as a go/no-go gate
From the inventoried data I write a first financial business case: future cost versus current cost, including the one-off investment and temporary transition costs. The outcome serves as a go/no-go moment, or a chance to re-evaluate earlier decisions before committing to execution.

## Related
- See `cloud-adoptie-framework-vier-pijlers.md` (this is the Insight pillar in action).
- See `cloud-transitie-posities.md` for the principles behind first-workload selection and cloud-native preference.

*Bron: geanonimiseerde aanpak uit een Salomon-IT klantopdracht (research and development organization (private research institute)).*

## Verwante notities

- [Bas: The 6 R's for Application Rationalization](bas-6-rs-cloud-migration.md)
- [Cloud adoption framework: four phased pillars](cloud-adoptie-framework-vier-pijlers.md)
- [Cloud-migration suitability checklist for client/server applications](cloud-migration-suitability-checklist-client-server-apps.md)
- [Positions I apply in a cloud transition](cloud-transitie-posities.md)
- [Criteria for Selecting the First Workload to Migrate](first-workload-selection-criteria.md)
- [Joint Inventory: Two Pairs of Eyes Beat One](joint-inventory-two-pairs-of-eyes.md)
- [Migration strategy framework: transition vs transformation, big-bang vs phased, build-clean-alongside](migration-strategy-decision-framework.md)
- [Transition/transformation engagement structure: intake, analyse, execute in plateaus](transition-transformation-engagement-structure.md)
