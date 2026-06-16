---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [avd, application, fslogix, app-masking, msix, dated]
layer: reference
gedateerd: ja
bron: nerdio-blog
---

# Application layering toward a zero-app golden image

Approaches Bas highlights for app delivery and ongoing image maintenance in AVD:

- **FSLogix App Masking** — apps live in the base image but rules determine which users see which apps; the rest are masked. Multiple apps can be grouped for consolidated access management. Nerdio can discover apps installed on a host pool image and configure these rules.
- **Layering solutions** (FlexApp One from Liquidware, MSIX App Attach from Microsoft) separate apps from the OS to simplify updates. App compatibility is never 100% with these, so trial and error remains. The ultimate end goal is zero applications in the golden image.
- **Browser/SaaS apps** are easier to maintain (vendor handles updates/security) but can still carry hidden dependencies like plugins.

For ongoing image management the options range from manual updates to full automation via SCCM, Intune, Azure DevOps pipelines, or PowerShell. Nerdio ships connectors for GitHub and Azure DevOps plus built-in management options. Whatever the route, testing is vital.

*Bron: Nerdio-content 'Top 5 things to consider before starting your AVD / Azure journey' (Blogs).*

## Verwante notities

- [AVD Application Management Strategy with Nerdio](avd-application-management-strategy-nerdio.md)
- [A six-pillar application management strategy for AVD](avd-application-management-strategy-six-pillars.md)
- [AVD/WVD Image Management Capabilities with Nerdio](avd-image-management-with-nerdio.md)
- [FlexApp One application layering, and how it compares to MSIX](flexapp-one-application-layering-explained.md)
- [MSIX AppAttach: what it is and why it matters](msix-appattach-explainer.md)
- [App layering that keeps the base image clean is the right model for AVD](positie-app-layering-keeps-the-image-clean.md)
- [Start from a fresh image rather than reusing legacy (Citrix) images](start-from-a-fresh-image.md)
