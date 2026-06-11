---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [troubleshooting, tool, scout, cdf, insight-services]
layer: reference
bron: inside-citrix-fma
---

# Citrix Scout: the aggregating troubleshooting tool

As of XenDesktop/XenApp 7.5, Citrix Scout is installed on Delivery Controllers by default. It aggregates many individual troubleshooting tools; its Utilities folder contains standalone applications (such as CDF Control) which run with full features as if downloaded separately. Scout uses CDF Control to perform the actual CDF tracing locally or on a remote machine.

Prerequisites for a CDF trace via Scout: local admin on the Delivery Controller and remote machines; WinRM, Remote Registry, and File and print sharing enabled on remote machines; all machines in the same domain; .NET Framework 3.5 SP1 or .NET 4.0; and PowerShell 2.0.

Scout's second big feature is collecting Data points (BIOS, OS, memory, drivers, registry keys, system/application event logs, Site/Farm info, WinRM settings, and more) from up to 10 machines. Collected data is analysed for corrective actions, saved as a .zip, then uploaded to Citrix Insight Services (an MD5 checksum confirms a successful upload). Reference: CTX130147.

## Verwante notities

- [Bas's troubleshooting philosophy: prepare in times of peace](bas-troubleshooting-philosophy-prepare-in-peace.md)
- [CDF Control, trace providers, and TMF file parsing](cdf-control-and-tmf-files.md)
- [Citrix Insight Services: automated log analysis and health checks](citrix-insight-services.md)
- [Citrix print troubleshooting tools](citrix-print-troubleshooting-tools.md)
- [Citrix printing troubleshooting and verification tools](citrix-printing-troubleshooting-tools.md)
- [Scout 3.0 swapped CDF-Control for Logman.exe (ETW)](citrix-scout-3-cdfcontrol-to-logman.md)
- [Citrix Diagnostic Toolkit and Supportability Pack collections](citrix-toolset-collections.md)
- [Director and built-in EdgeSight](director-monitoring-tool.md)
- [Director SCOM and Insight Services integration](director-scom-and-insight-services-integration.md)
- [Parsing CDF traces: .etl files, TMF files, public vs private](etl-parsing-tmf-files-public-private.md)
- [HDX Monitor: HDX diagnostics tool](hdx-monitor-tool.md)
- [Don't forget old-school tools (NetStat, Ping, Tracert, Telnet)](old-school-troubleshooting-tools.md)
- [PortICA / picaSvc2.exe: the critical VDA ICA service](portica-picasvc2-service.md)
- [Print-related troubleshooting tools (Print Detective, UPS Cert Tool, StressPrinters)](print-troubleshooting-tools.md)
- [Service logging in XenDesktop (command-line vs Scout)](xendesktop-service-logging.md)
