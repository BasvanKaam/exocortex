---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-10
tags: [aws, appstream, application-streaming, euc]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# How AWS AppStream 2.0 streams apps (2019)

How it worked then: AppStream streams applications from the AWS Cloud to a user's device. It works with 'Fleets', a Fleet consisting of an image (built with the AppStream image builder) and one or more instances (VMs) that launch the image and stream apps. Apps are installed onto an image; you pick custom or pre-defined images optimized for compute, memory or graphics. You configure network, session settings (on-demand, always-on, max duration, timeout), min/max streaming instance capacity, and scale-out/scale-in policies. The cloud-native part (auto-scaling, policies) is hard to replicate on-premises.

*Bron: blogpost 'AWS launched AppStream 2.0, here's how Liquidware adds some 'magic' on top' (2019-05-08), basvankaam.com.*

## Verwante notities

- [Amazon WorkSpaces architecture (2013 preview)](amazon-workspaces-2013-architecture.md)
- [Application layering: abstract the app from the OS](app-layering-abstraction-durable-concept.md)
- [Cloud-native does not fix application management](appstream-management-not-solved-positie.md)
- [Reserved, Scheduled and Spot instances as AWS cost levers](aws-instance-purchasing-models-cost.md)
- [Universal Print: moving print to the M365 cloud](universal-print-cloud-print-concept.md)
