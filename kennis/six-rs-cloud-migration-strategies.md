---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-16
tags: [cloud-migration, strategy, modernization, framework]
layer: reference
gedateerd: nee
bron: inside-citrix-book
---

# The 6 Rs of cloud migration

A taxonomy for deciding what to do with each application when moving to the cloud. Each application is assessed and assigned one of six dispositions:

- **Rehost** (lift-and-shift): move the app to the cloud unchanged. Fastest, lowest immediate effort, but no cloud-native benefit yet.
- **Replatform**: make limited adjustments so the app runs better in the cloud (e.g. swap to a managed database) without rewriting it.
- **Refactor / re-architect**: rewrite the app to exploit cloud capabilities such as elasticity and scalability. Highest effort, highest long-term payoff.
- **Repurchase**: drop the existing software and move to a different, cloud-based (typically SaaS) product.
- **Retain**: deliberately keep the app on-premises because it is not (yet) suitable for migration.
- **Retire**: decommission an app that is no longer needed.

Use it as a per-app decision filter during portfolio assessment rather than treating the whole estate as one migration.

*Bron: Inside Citrix (2016), 'Hoofdstuk 8 - Begrippenlijst (cloud-migration glossary)'.*

## Verwante notities

- [Bas: The 6 R's for Application Rationalization](bas-6-rs-cloud-migration.md)
- [There is no such thing as a cloud strategy](cloud-is-not-a-strategy.md)
- [Migration strategy framework: transition vs transformation, big-bang vs phased, build-clean-alongside](migration-strategy-decision-framework.md)
- [SCAF - Step-Cloud Adoptie Framework](scaf-step-cloud-adoptie-framework.md)
- [SCAF: Step-Cloud Adoption Framework and its toolkit](scaf-step-cloud-adoption-framework.md)
