---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [nerdio, avd, framework, training-method, adoption]
layer: reference
gedateerd: nee
bron: nerdio-training
---

# Nerdio Enterprise Optimization Journey (12-step framework)

The spine Bas uses to structure the Enterprise Training Camp: a sequential journey that takes an admin from scoping to a fully automated, iterating environment. The order is the teaching order and the implementation order.

1. Scope your environment - which apps users need, which are generally applicable vs workgroup-specific, expected user behavior. Use logs to scope existing environments; work with developers to scope new ones.
2. Configure user experience settings - centralized, scalable templates for FSLogix and RDP Settings Profiles that define session behavior.
3. Create Desktop Images - build a tool for rapid deployment; scope per-workgroup needs, consolidate overlap, keep images light so updates and patches stay fast.
4. Implement automations - inventory and consolidate orphaned scripts, generalize them, use secure variables, connect GitHub/DevOps, build scripts natively in Nerdio.
5. Create host pools - select the base Desktop Image, assign UX settings, customize deployment properties.
6. Leverage UAM - policy-driven app management; inventory general vs unique apps, decide what can be automated, create/connect an in-house repository.
7. Configure Auto-scale - use profiles for consistent centralized config, add capacity when it counts and remove it when things slow down.
8. Extend beyond AVD with UEM (Intune/endpoints).
9. Deliver updates via the Foundations pipeline.
10. Onboard new departments using the Foundations framework.
11. Make iterative changes rather than major projects.
12. Implement the Nerdio API to extend into the wider tech stack.

Guiding principle that recurs: make iterative changes, not big-bang projects. Onboard new departments/customers by reusing the same Foundations framework rather than rebuilding.

*Bron: Nerdio-content 'NEW_v3.0 Enterprise Training Camp_PRESENTER' (Training).*

## Verwante notities

- [Idea: 30-day Nerdio engineer bootcamp framework](idee-nerdio-30-day-engineer-bootcamp.md)
- [Idea: Nerdio Fusion - a merged event format](idee-nerdio-fusion-merged-event-format.md)
- [Method: Bas's Nerdio lab-guide template convention](method-nerdio-lab-guide-template.md)
- [Nerdio Adoption & Management Framework: Five Foundational Elements](nerdio-adoption-management-framework.md)
- [Nerdio autoscaling engine: pooled hostpool scaling logic](nerdio-autoscaling-engine-pooled-hostpools.md)
- [Nerdio image lifecycle: import, update, re-image](nerdio-image-lifecycle-import-update-reimage.md)
- [Scoping desktop images: what to avoid on an image source VM](nerdio-image-source-vm-scoping-pitfalls.md)
- [Nerdio Innovation Day vs Enterprise Training Camp](nerdio-innovation-day-vs-enterprise-training-camp.md)
- [Unified Application Management: four key concepts](nerdio-uam-four-key-concepts.md)
- [NME persists machine names across reimage/rebuild](nme-hostpool-naming-persistence.md)
- [Iterate, don't run big-bang projects](positie-iterative-changes-over-big-projects.md)
