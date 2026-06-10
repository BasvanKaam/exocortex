---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [sizing, design, project-accelerator, citrix-consulting]
layer: reference
bron: inside-citrix-fma
---

# Citrix Project Accelerator: web-based design guidance

Citrix Project Accelerator (project.citrix.com) is a web-based application that guides you through questions, requirements, and common design choices, founded on Citrix Consulting practices and regularly updated. At the book's time of writing it supported up to XenDesktop/XenApp 7.5.

Workflow:
- Assess Phase: a five-step definition of your organisation (business info, project type, user groups and applications, then linking applications to user groups). It asks about industry, number of users, business priorities (BYOD, work-from-anywhere, cost reduction, better desktop management) and existing Citrix skill sets. This is the most important phase; per the FMA fact it takes roughly 30-60 minutes when thought through beforehand.
- Design Phase: makes technical recommendations on products, the FlexCast delivery model, hardware/sizing (including CPU overcommit suggestions), IOPS, and image provisioning/management (PVS vs MCS, preferred storage). All suggestions are manually adjustable.
- Documents section: provides an Architecture diagram and a Sizing and deployment plan based on your inputs.

## Verwante notities

- [Bas on CPU over-commit and user baselines (light/medium/heavy)](cpu-overcommit-and-user-baselines.md)
- [FlexCast delivery technology, worker types and delivery models](flexcast-delivery-models-and-worker-types.md)
- [Machine Creation Services (MCS): integrated single-image delivery](machine-creation-services-overview.md)
- [Citrix Provisioning Services (PVS) overview](provisioning-services-overview.md)
- [Bas on sizing: there is no 'one size fits all', and don't overdo it](sizing-no-one-size-fits-all.md)
- [Sizing resources: XenDesktop Design Handbook and community calculators](sizing-resources-and-handbook.md)
- [Bas's troubleshooting and sizing philosophy](troubleshooting-and-sizing-philosophy.md)
