---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [cloud-pc, windows-365, nerdio-manager, image-management, scripted-actions, msp]
layer: reference
gedateerd: ja
bron: nerdio-blog
---

# Where Nerdio adds value on top of native Cloud PC

Bas's reusable argument for why a management layer matters on top of native Cloud PC:

- **Unified console.** Manage MEM-managed Cloud PC, self-service Cloud PC, and AVD from one interface, single- or multi-tenant, including the Cloud PC network connections (normally split between Intune and the Azure portal).
- **Image management.** Native Cloud PC has no real image-based software deployment without a third-party tool. Nerdio brings AVD-grade image management to Cloud PC: automated, scheduled software deployment, updating and patching of MEM-managed machines, side by side with AVD.
- **Profile management.** Image-based deployment brings profile management; automated FSLogix setup handles it where used.
- **Re-provisioning and restart.** Drive (re)provisioning and restarts of Cloud PC VMs directly from the console, including for self-service Cloud PCs that otherwise have no admin portal.
- **Scripted Actions on Cloud PC from day one.** 100% PowerShell-based, available on Cloud PC environments as well as AVD.
- **Everything-else around the desktop.** Spinning up a Cloud PC or AVD host is the easy part; the value is in users, identity, backup, networking, monitoring, autoscaling, VPNs, and the other non-AVD VMs — for one environment or hundreds.
- **Migration both ways.** The console enables AVD-to-Cloud-PC and back so each user lands on the right desktop type in the most cost-effective way.

Note: MSIX app attach was not supported on Cloud PC at the time of writing (version-specific).

*Bron: Nerdio-content 'How Nerdio Enhances the Provisioning and Management of Cloud PC' (Blogs).*

## Verwante notities

- [AVD/WVD Image Management Capabilities with Nerdio](avd-image-management-with-nerdio.md)
- [Cloud PC: MEM-managed vs self-service (durable distinction)](cloud-pc-mem-managed-vs-self-service.md)
- [Cloud PC vs AVD: a four-lens decision framework](cloud-pc-vs-avd-decision-framework.md)
- [Nerdio image lifecycle: import, update, re-image](nerdio-image-lifecycle-import-update-reimage.md)
- [Where Nerdio adds value on top of native Cloud PC](nerdio-value-on-top-of-cloud-pc.md)
- [What Nerdio Scripted Actions are](nmw-scripted-actions-explainer.md)
- [AVD and Cloud PC go hand in hand, pick per use case](positie-avd-en-cloud-pc-gaan-hand-in-hand.md)
- [Windows 365 and AVD Are Complementary, Not Competing](positie-w365-and-avd-coexist.md)
- [Simplicity comes at the cost of flexibility](simplicity-costs-flexibility.md)
- [Windows 365 License Optimization: The Three Levers](w365-license-optimization-method.md)
