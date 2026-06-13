---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [nerdio, uam, application-management, avd, intune, explainer]
layer: reference
gedateerd: ja
bron: nerdio-training
---

# Unified Application Management: four key concepts

The reusable taxonomy Bas uses to teach UAM as a single pane of glass across AVD, Windows 365 Cloud PCs and physical (Intune) devices. Four questions structure every UAM decision:

1. Applications - what installation formats need to be delivered? EXE, MSI, MSIX, App attach (CIM, VHD), APPX, BURN, INNO, MSSTORE, NULLSOFT, Portable, ZIP (single file), PWA, WIX.
2. Targets - where will apps be installed? Pooled AVD host pools, personal AVD desktops, specific pools, servers, by user/group; or Intune-connected/enrolled devices by user, group or device group.
3. Repositories - where are apps stored and who maintains them? Microsoft Store, WinGet community, private/custom repo, Google Play, iOS Store. Software publishers maintain packages (often free) and packages are commonly digitally signed.
4. Deployment technologies - how are apps delivered to clients?
   - WinGet: Azure-connected (virtual) via native Azure extensions; Intune-connected (physical) via Intune pushing scripts for WinGet commands.
   - SCCM: same Azure-extension / Intune-script split.
   - Shell apps: customized script packages; can call WinGet if needed; for complex deployments or where WinGet isn't practical.
   - MSIX / App attach: virtual only; attaches the app package to the VM.

Why it matters (benefits framing): faster response to app updates and vulnerabilities (security), less manual management via policy-based deployment (time), and reduced tool sprawl (cut down Chocolatey/Ninite/etc.). dated:true - format list and deployment mechanics are product-version-specific.

*Bron: Nerdio-content 'PRESENTER_Enterprise_Foundations_v4.0' (Training).*

## Verwante notities

- [AVD Application Management Strategy with Nerdio](avd-application-management-strategy-nerdio.md)
- [A six-pillar application management strategy for AVD](avd-application-management-strategy-six-pillars.md)
- [Idea: Nerdio vs shadow IT](idee-nerdio-shadow-it-governance.md)
- [Nerdio Adoption & Management Framework: Five Foundational Elements](nerdio-adoption-management-framework.md)
- [Nerdio Enterprise Optimization Journey (12-step framework)](nerdio-enterprise-optimization-journey.md)
- [Windows in the cloud as a Living Persona](windows-in-the-cloud-as-living-persona.md)
