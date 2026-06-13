---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [cloud-pc, windows-365, licensing, intune, m365, avd]
layer: reference
gedateerd: ja
bron: nerdio-blog
---

# Cloud PC licensing requirements (durable)

From Bas's CPC explainer draft, the licensing essentials (same Windows subscription requirement as AVD):

- You need a **Windows 10/11 Enterprise subscription** license. A physical-device/OEM license does not qualify; only an M365 subscription to Windows works for Cloud PCs.
- SKUs that include the Windows Enterprise subscription: **M365 Business Premium, E3, E5, and Windows 10 Enterprise E3/E5/VDA**.
- For **MEM-managed** Cloud PCs you additionally need an **Intune license** per user. Intune is bundled in M365 E3, E5, and Business Premium, or can be bought standalone.
- **Self-service** Cloud PCs need no Intune license.
- Because Cloud PC is part of M365, it is purchased through the same channels (E3/E5) organizations already use for AVD. Subscription-based, no minimums; if it does not work out you hand the licenses back to Microsoft.

*Bron: Nerdio-content 'NEEDS EDITS - What is and how Nerdio enhances CPC' (Blogs).*

## Verwante notities

- [M365 E3 already entitles you to AHU for WVD](ahu-entitlement-via-m365-e3.md)
- [Cloud PC: MEM-managed vs self-service (durable distinction)](cloud-pc-mem-managed-vs-self-service.md)
- [Cloud PC: MEM-managed vs self-service flavours](cloud-pc-mem-managed-vs-self-service-2.md)
- [Cloud PC vs AVD: a four-lens decision framework](cloud-pc-vs-avd-decision-framework.md)
- [Nerdio consumption-based licensing model](nerdio-licensing-model.md)
- [Windows 365 Cloud PC: What It Is and How It Differs from AVD](w365-cloud-pc-vs-avd-fundamentals.md)
- [Windows 365 License Optimization: The Three Levers](w365-license-optimization-method.md)
- [Windows 365 Cloud PC - Business vs Enterprise](windows-365-business-vs-enterprise.md)
- [Why Windows 365 enablement needs Global Admin (org consent)](windows-365-enablement-permissions.md)
