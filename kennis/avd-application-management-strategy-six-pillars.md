---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [nerdio, avd, application-management, msix-app-attach, fslogix, image-management, scripted-actions]
layer: reference
gedateerd: ja
bron: nerdio-blog
---

# A six-pillar application management strategy for AVD

His comprehensive framework for deploying and continuously maintaining applications on AVD, organized as six layers:

1. Unified Application Management (UAM): connect one or more application repositories to centralize deploy/update/maintain across the full app lifecycle. The Winget community repository (Microsoft-managed, thousands of vendor-distributed packages) links by default; you can also create private repositories for corporate apps. Configurable deployment policies plus deployment-status and compliance insight. Repository types span manual file-share/network-drive deployment, GPO-based deployment, Configuration Manager (SCCM), installation into master images (VDI and physical), app streaming/virtualization, and scripted installs via third-party tools. The objective: deploy any Windows application to any Windows device via one centralized catalog.

2. Image Management: golden images as standardized, customizable templates per user group/department. The whole workflow (install apps, security updates, patches, apply image to a test hostpool) can be fully automated and scheduled hourly/daily/weekly/monthly, including an 'x days after Patch Tuesday' option. Hostpool updates: scheduled, repeated, advance user reboot notifications, drain mode for graceful session disconnect, parallel re-imaging for large hostpools, and no NIC changes during update (no DNS/IP changes). Optional integration with SCCM, Ivanti, or DevOps.

3. MSIX AppAttach: attach applications to AVD sessions on demand instead of traditional installs, enabling rapid provisioning. Managed without PowerShell via GUI, including certificate management; versioning lets you update without disrupting users, with optional rollback.

4. Scripted Actions: automated scripts running predefined tasks across single or multiple AVD sessions (deploy apps, apply patches/updates, configure settings); integrate into the image-management workflow to further automate.

5. FSLogix: profile and data management by virtualizing user profiles for a consistent cross-device experience and fast logins. Also provides application masking: include multiple apps on one image, then use masking rules to control which users/groups can see and access specific apps regardless of being on the same hostpool.

6. Third-party integrations: e.g. Rimo3 (imports apps from SCCM, tests AVD suitability and multi-session capability, modernizes MSIX, exports to Nerdio), ControlUp (real-time end-to-end EUC monitoring and remediation, UX focus), and Liquidware FlexApp ONE (assign/attach portable, self-contained FlexApp apps hosted in Azure to AVD workspaces with no extra agent or console).

*Bron: Nerdio-content 'Streamlining application delivery via AVD - A Comprehensive Application Management Strategy' (Blogs).*

## Verwante notities

- [Application layering toward a zero-app golden image](application-layering-zero-apps-in-golden-image.md)
- [AVD Application Management Strategy with Nerdio](avd-application-management-strategy-nerdio.md)
- [AVD/WVD Image Management Capabilities with Nerdio](avd-image-management-with-nerdio.md)
- [FlexApp One application layering, and how it compares to MSIX](flexapp-one-application-layering-explained.md)
- [MSIX AppAttach: what it is and why it matters](msix-appattach-explainer.md)
- [Setting up MSIX App Attach v2 in Nerdio and publishing apps](msix-appattach-v2-publish-nerdio.md)
- [Unified Application Management: four key concepts](nerdio-uam-four-key-concepts.md)
- [App layering that keeps the base image clean is the right model for AVD](positie-app-layering-keeps-the-image-clean.md)
- [Call them traditional Windows apps, not legacy, and AVD keeps them alive](position-traditional-not-legacy-windows-apps.md)
