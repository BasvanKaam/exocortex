---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, director, edgesight, monitoring, netscaler, hdx-insight]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# EdgeSight folded into Citrix Director (XD7)

How it worked in XenDesktop 7. EdgeSight as a standalone product was EOL'd; its technology and branding were absorbed into Citrix Director. Director is a real-time, web-based troubleshooting console (used mainly by helpdesk) and ships with *every* edition, giving live health monitoring with 7 days of data.

EdgeSight functionality was gated behind licenses:
- All editions: Director real-time monitoring, 7 days of data.
- XD7 Platinum: EdgeSight performance management, up to a year of historical data (needs a SQL database).
- XD7 Platinum + NetScaler Enterprise: adds network analysis with 60 minutes of network data.
- XD7 Platinum + NetScaler Platinum: network analysis with unlimited network data.

Network analysis uses NetScaler HDX Insight and requires the new XD7-era Receiver for Mac/Windows. Director can monitor older/lower VDAs, but the Controller must be on XD7 and some metrics won't be collected for the older VDAs.

*Bron: blogpost 'XenDesktop 7 editions explained' (2013-06-27), basvankaam.com.*

## Verwante notities

- [Intelligent Configuration Validation and built-in Profile Management](excalibur-built-in-config-validation.md)
- [Citrix's problem is integration and focus, not lack of products](positie-citrix-should-integrate-not-just-build.md)
