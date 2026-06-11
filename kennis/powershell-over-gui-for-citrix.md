---
type: positie
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, powershell, studio, director, opinion]
bron: basvankaam-blog
---

# Prefer PowerShell over the GUI for Citrix FMA work

Stance (March 2015): Bas consistently nudges admins toward PowerShell over the Studio/Director GUI. Director's alerts are too shallow ('it won't tell you what is wrong or where to look for answers'), Director doesn't monitor all FMA services by default, and PowerShell both diagnoses better and unlocks 'a whole bunch of extra configuration options not available using just Studio.'

This fits a recurring theme in his writing: understand and operate the layer beneath the GUI. He recommends baking service-health Get- checks into a personal PowerShell profile so verification happens automatically. A clear, durable opinion about working close to the engine rather than the dashboard.

*Bron: blogpost '12 services that make up the Citrix XenDesktop Flex Management Architecture' (2015-03-26), basvankaam.com.*

## Verwante notities

- [Companies overspend on StoreFront branding](branding-storefront-overrated-effort.md)
- [Critique: why isn't this in the GUI? (web.config friction)](build-it-into-the-gui-position.md)
- [Check FMA service health with PowerShell, not just Director](check-fma-services-with-powershell.md)
- [Citrix Site policies: Entitlement, Assignment, Site Access](citrix-site-policies-powershell.md)
- [How PowerShell DSC works: authoring, MOF, push and pull](desired-state-configuration-basics.md)
- [Director and built-in EdgeSight](director-monitoring-tool.md)
- [The FMA core services and how they communicate](fma-services-complete-overview.md)
- [The FMA's 10 (or 12) primary services and their roles](fma-twelve-services-rundown.md)
- [Hiding apps (Limit Visibility) vs hiding desktops (PowerShell entitlement filter)](limit-visibility-vs-entitlement.md)
- [Delivering Linux shared hosted desktops: controller, catalog and delivery group setup](linux-vda-controller-and-catalog-config.md)
- [Multi-type licensing in XenDesktop/XenApp 7.14](multi-type-licensing-714.md)
- [Never skip the basics: start troubleshooting at the event logs](never-skip-the-basics-event-logs.md)
- [Positie: Citrix was inexplicably late adding delegated admin to XenDesktop](positie-citrix-late-with-xendesktop-delegated-admin.md)
- [Using PowerShell to check FMA service states](powershell-fma-service-checks.md)
- [StoreFront's powerful features shouldn't be locked behind web.config](storefront-config-should-be-in-the-gui.md)
- [Everything you do in Studio is PowerShell underneath](studio-is-powershell-underneath.md)
- [Use health-check tooling proactively, not only when things fall apart](use-monitoring-proactively-not-when-it-breaks.md)
