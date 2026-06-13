---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [avd, application-management, msix-appattach, fslogix, image-management, uam, dated]
layer: reference
gedateerd: ja
bron: nerdio-blog
---

# AVD Application Management Strategy with Nerdio

Bas's framing of application management on AVD as an ongoing lifecycle (deploy, update, maintain), with Nerdio providing the tooling. Most underlying mechanics (MSIX AppAttach, FSLogix, image management) are already covered in the brain; this captures the strategic structure and the few durable framings.

## The six pillars Bas uses to structure the story
1. Unified Application Management (UAM): one centralized catalog, connect one or multiple repositories. Winget community repo linked by default (Microsoft-managed, thousands of vendor-distributed packages). Private repositories for corporate apps. Stated objective: deploy any Windows application to any Windows device via a simple centralized catalog. Repository types span file shares/network drives, group policy, SCCM, master-image installs (VDI and physical), app streaming/virtualization, and scripted 3rd-party installs.
2. Image Management: golden images as standardized, customizable templates; full GUI-driven workflow from app install through (security) updates/patches to applying the image to (test) hostpools. Scheduling hourly/daily/weekly/monthly plus an 'x days after Patch Tuesday' option. Optional integration with SCCM, Ivanti, DevOps. Updates put machines into drain mode for graceful logoff, notify users of reboots, re-image multiple machines in parallel, and preserve the NIC so there are no DNS/IP changes.
3. MSIX AppAttach: attach apps to AVD sessions on demand, managed via GUI (no PowerShell) including certificate management; versioning lets you update without disruption, rollback optional.
4. Scripted Actions: predefined automated scripts across single or multiple AVD sessions; integrate into the image-management workflow.
5. FSLogix: profile/data virtualization for consistent experience and fast logins; application masking (available directly from Nerdio) lets one image hold many apps while masking rules control which apps each user/group sees, even within the same hostpool.
6. Third-party integrations: extend AVD with existing software investments.

The reusable structural idea: present application management as a continuous cycle, then walk the same six capability buckets.

*Bron: Nerdio-content 'Applications' (Blogs).*

## Verwante notities

- [Application layering toward a zero-app golden image](application-layering-zero-apps-in-golden-image.md)
- [A six-pillar application management strategy for AVD](avd-application-management-strategy-six-pillars.md)
- [FlexApp One application layering, and how it compares to MSIX](flexapp-one-application-layering-explained.md)
- [MSIX AppAttach: what it is and why it matters](msix-appattach-explainer.md)
- [Nerdio image lifecycle: import, update, re-image](nerdio-image-lifecycle-import-update-reimage.md)
- [Unified Application Management: four key concepts](nerdio-uam-four-key-concepts.md)
- [App layering that keeps the base image clean is the right model for AVD](positie-app-layering-keeps-the-image-clean.md)
