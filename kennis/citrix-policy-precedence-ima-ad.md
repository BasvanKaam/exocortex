---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, group-policy, ima, xenapp, policy-precedence]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Citrix policy precedence: IMA vs Citrix AD vs normal AD policies

How it worked then (XenApp 6/6.5). Three policy systems coexisted: IMA-based Citrix policies, Citrix AD policies (available from XenApp 6.0, configured in GPMC after installing the Delivery Services Console / App Center bits so a Citrix container appears), and normal Microsoft AD policies. Citrix recommended using only one of IMA-based or Citrix AD policies for farm policies, not both.

Precedence rules:
- AD policies (Citrix or normal) take precedence over IMA-based policies.
- A Citrix AD policy applied after an IMA policy overwrites it (both are Citrix policies): e.g. IMA enables clipboard mapping, Citrix AD disables it, result is disabled.
- A normal AD policy CANNOT overwrite a Citrix-specific setting even with the same intent: IMA enables clipboard mapping, normal AD 'disables' it, result stays enabled.
- But a normal AD policy CAN win when it targets the same outcome via a different setting: a Citrix server idle timer of 5 min plus a normal-AD RDS idle session limit of 10 min results in 10 min.

To see applied Citrix AD policies, run GPResult from within GPMC (Group Policy Results Wizard) with the XenApp bits installed; command-line GPResult/RSOP does not show Citrix AD policies on a XenApp 6 server (known issue).

*Bron: blogpost 'Troubleshooting one on one' (2013-01-17), basvankaam.com.*

## Verwante notities

- [Troubleshooting tip #1: document what you've done](document-your-troubleshooting.md)
- [FMA vs IMA: no Zones, no Data Collectors, no Local Host Cache (2013)](fma-vs-ima-no-zones-no-lhc.md)
- [IGEL UMS: central thin client management via profiles and directories](igel-ums-thin-client-management.md)
- [IMA-to-FMA terminology: Farm to Site, Data Collector to Delivery Controller](ima-to-fma-terminology-map.md)
- [Skip XenApp 6.0, go straight to 6.5 (April 2013)](skip-xenapp-60-go-straight-to-65.md)
- [Detecting XenApp session sharing via the ICA Session registry key](xenapp-session-sharing-registry-states.md)
