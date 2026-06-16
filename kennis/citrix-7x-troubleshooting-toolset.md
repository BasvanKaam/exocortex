---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, troubleshooting, tool, scout, cdf, director]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# The Citrix XenDesktop/XenApp 7.x troubleshooting toolset

How it worked then (7.x era, 2014):

- XDDBDiag: consistency check and connectivity verification on the XenDesktop database; outputs CSV in a zip.
- XDPing: command-line connectivity tracer; checks config on Broker and VDA machines, locally or remotely.
- HDX Monitor 3.x: diagnostics on HDX technologies (also supports XenApp 6.5).
- Citrix Scout: installed by default as of 7.5; aggregates CDF Control, XDPing, service logging, and collects data points (BIOS, OS, memory, drivers, registry, event logs, Site/Farm info) for upload to Citrix Insight Services (TaaS).
- CDF Control: Citrix Diagnostic Facility trace capture; standalone or inside Scout.
- Print Detective: enumerates and can delete print drivers.
- Director: monitoring with Helpdesk and Administrative views, historical data (1 hour / 24 hours / 7 days), logon-duration breakdown, shadowing.
- Citrix Insight Services (taas.citrix.com): auto-analyzes uploaded logs against hundreds of known issues with red/yellow/green prioritization.

Service logging note: Scout couldn't log certain services (e.g. the Broker Agent / VDA); the command-line gave access to all services.

*Bron: blogpost 'Troubleshooting Citrix XenDesktop & XenApp 7.x ? Read this !' (2014-10-20), basvankaam.com.*

## Verwante notities

- [CDF Control, trace providers, and TMF file parsing](cdf-control-and-tmf-files.md)
- [How CDF tracing works: providers, modules, trace messages](cdf-tracing-providers-modules-messages.md)
- [Citrix Scout, TaaS and Insight Services as the 2015 troubleshooting chain](citrix-scout-taas-insight-services.md)
- [A candid critique of Citrix support response times](citrix-support-keep-them-on-their-toes.md)
- [Director and built-in EdgeSight](director-monitoring-tool.md)
- [Parsing CDF traces: .etl files, TMF files, public vs private](etl-parsing-tmf-files-public-private.md)
- [HDX Monitor: HDX diagnostics tool](hdx-monitor-tool.md)
- [XDDBDiag: XenDesktop Database Diagnostic tool](xddbdiag-tool.md)
- [XDPing: XenDesktop connectivity and configuration checker](xdping-tool.md)
