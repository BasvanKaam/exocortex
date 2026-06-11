---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, vdi-in-a-box, xendesktop, comparison, vdi]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# VIAB vs XenDesktop: simplicity vs flexibility tradeoffs (2013)

Bas's side-by-side:
- FlexCast: XenDesktop delivers many models (Hosted Shared, Hosted VDI, Streamed VDI, Local VM, on-demand apps); VIAB does VDI only.
- Authentication: both support AD and smart cards, but VIAB also supports Workgroup (local DB) environments - a plus for small shops. XenDesktop requires AD.
- Automation: XenDesktop has an extensive PowerShell SDK; VIAB keeps it to simple wizards.
- Policies: same HDX policy engine, but VIAB requires policies stored in AD (XenDesktop can store them in the site DB).
- Images: XenDesktop uses PVS/MCS with versioning; VIAB imports externally-created VMs with no versioning.
- HA: both support shared storage; XenDesktop has central-database HA requirements, VIAB uses local config files per host.

The recurring conclusion: 'it all depends' - pick complexity only where the business case needs it.

*Bron: blogpost 'Project Curacao complete overview' (2013-05-14), basvankaam.com.*

## Verwante notities

- [FlexCast delivery technology, worker types and delivery models](flexcast-delivery-models-and-worker-types.md)
- [On over-engineering HA: simplicity often wins, but it all depends](ha-it-all-depends.md)
- [Server 2012 R2 data dedup and the VDI separation rule](server-2012-r2-dedup-for-vdi.md)
- [Categorize users before choosing a desktop model](user-categorization-for-desktop-design.md)
- [VDI-in-a-Box: a single all-in-one VDI appliance (how it worked)](vdi-in-a-box-all-in-one-appliance.md)
- [VDI-in-a-Box: the simplified all-in-one VDI appliance](vdi-in-a-box-architecture.md)
- [VDI-in-a-Box served a real niche: simple, cheap, small-scale VDI](vdi-in-a-box-simple-vdi-niche.md)
- [VIAB isn't for everyone, but with the right business case it just feels right (May 2013)](viab-given-the-right-business-case-it-feels-right.md)
- [Simplicity is a feature, not a drawback (VIAB)](viab-simplicity-is-strength-position.md)
- [WorkspacePod is not an honest VIAB replacement (yet)](workspacepod-not-a-viab-replacement.md)
- [XenDesktop 7 Host Infrastructure and what it unlocks](xendesktop-host-infrastructure-mcs-pvs.md)
