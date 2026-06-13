---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [avd, security, shared-responsibility, nerdio, cheat-sheet]
layer: reference
gedateerd: nee
bron: nerdio-blog
---

# AVD Shared Responsibility: Who Secures What

Bas frames every AVD security conversation by first answering "who is responsible for what?" His responsibility split:

**Customer is responsible for:** identity, the user, app security, the session host OS, deployment configuration, the Nerdio management console and its components, and network controls.

**Microsoft / not the customer:** the virtualization control plane, physical hosts, physical network, and the physical datacenter.

The point is that the cloud and management vendors cover the lower stack, but identity, OS, apps, network and the management console remain squarely the customer's job, which is exactly where most of the security checklist work lives.

*Bron: Nerdio-content 'Nerdio - AVD security cheat sheet' (Blogs).*

## Verwante notities

- [AVD security cheat sheet: the six-category framework](avd-security-cheat-sheet-framework.md)
- [AVD Security Checklist by Layer (Bas's Cheat Sheet)](avd-security-checklist-by-layer.md)
- [Hardening the Nerdio Manager Console Itself](nerdio-manager-hardening-checklist.md)
- [Nerdio Is Not Secure Out of the Box, So Always Harden](positie-nerdio-not-secure-out-of-the-box.md)
- [Nerdio Manager Is an Orchestration Layer, Not a Security Product](position-nerdio-is-orchestration-not-a-security-product.md)
- [Shared Responsibility Model (Restaurant Analogy)](shared-responsibility-model-restaurant-analogy.md)
