---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [nerdio, avd, framework, foundations, automation]
layer: reference
gedateerd: nee
bron: nerdio-training
---

# Nerdio Adoption & Management Framework: Five Foundational Elements

The core message Bas drives in the camp: get five foundations right once, then host pool creation plus auto-scale does the rest ("Create a host pool, configure and enable Auto-scale, Done - Nerdio deploys hosts").

The five foundational elements:
1. Create the image source VM - a central point for managing updates; update it on a scheduled basis via automations.
2. Define user experience settings - configure FSLogix and RDP Profile Settings.
3. Implement automations / scripted actions - generalized scripts with variables.
4. Create UAM policies - install and update applications with policies.
5. Create host pools and configure auto-scaling - auto-scale leverages your foundations to automate host deployment and management.

The mental model he repeats: the image source VM is the engine. It is the single target for changes, patches and updates; from it you build a Desktop Image (versioned, used to deploy hosts one-to-many and scale rapidly); automations layer on custom app installs, customizations and Intune policies. Get the foundations laid and ongoing operations collapse to host-pool-plus-auto-scale.

*Bron: Nerdio-content 'NEW_v3.0 Enterprise Training Camp_PRESENTER' (Training).*

## Verwante notities

- [Idea: 30-day Nerdio engineer bootcamp framework](idee-nerdio-30-day-engineer-bootcamp.md)
- [Involve and educate users early or adoption fails](involve-users-early-for-adoption.md)
- [Nerdio autoscaling engine: pooled hostpool scaling logic](nerdio-autoscaling-engine-pooled-hostpools.md)
- [Nerdio Enterprise Optimization Journey (12-step framework)](nerdio-enterprise-optimization-journey.md)
- [Scoping desktop images: what to avoid on an image source VM](nerdio-image-source-vm-scoping-pitfalls.md)
- [Unified Application Management: four key concepts](nerdio-uam-four-key-concepts.md)
- [NME image management: prefer the compute gallery over the source VM](nme-image-management-gallery-vs-source-vm.md)
- [Iterate, don't run big-bang projects](positie-iterative-changes-over-big-projects.md)
- [Windows in the cloud as a Living Persona](windows-in-the-cloud-as-living-persona.md)
