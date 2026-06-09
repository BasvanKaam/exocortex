---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-09
tags: [business-case, hybrid-cloud, migration-planning, modern-workplace]
layer: rich
bron: van-de-basis-tot-meester-in-de-cloud
---

# Bas's mini business case: the current-vs-possible mapping table

When asked to think about the next step for the 'modern workplace', Bas's recommended starting point for a first mini business case is a two-column table that maps the current (on-prem) situation against a possible (hybrid) approach. You have to start somewhere, and forcing yourself to draft an overview already begins to give the plan shape.

His worked example (product names are easily swapped to fit the situation):
- Solution X for apps/desktops -> Microsoft AVD + IaaS
- Exchange on-premises -> Microsoft 365 (E3) / Exchange Online
- Domain Controllers (x2) -> Entra ID + Intune
- On-prem financial application server -> IaaS plus SaaS
- SQL server for the financial app -> PaaS
- File / Print server -> Azure Files / OneDrive / Universal Print
- Network connectivity -> Azure ExpressRoute
- Fat clients (laptops) -> Laptops / Intune
- Azure MFA -> Azure MFA
- Back-up/infinite retention -> 'Nader uit te werken' (to be worked out)
- Other applications -> Laptop + AVD + Intune

Bas notes you probably haven't made final XaaS choices yet, but you're fairly sure this is the route you'll take. He suggests building these tables in PowerPoint so they're easy to present when needed. This particular example, he says, is one that occurs very frequently today for a range of reasons.

## Bron-citaten (NL, verbatim)

> je moet ergens beginnen
>
> Door dit soort overzichten en tabellen te creëren in PowerPoint kun je ze eenvoudig presenteren, wanneer nodig.
