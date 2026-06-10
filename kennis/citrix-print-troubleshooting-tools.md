---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [printing, troubleshooting, tools, scout, print-detective]
layer: reference
bron: inside-citrix-fma
---

# Citrix print troubleshooting tools

Useful print/diagnostic tools Bas lists:
- Print Detective: enumerates all printer drivers (with driver-specific info) on a Windows machine, can delete specified drivers, logs, and has a CLI.
- Citrix Scout: all-purpose tool run from a single Delivery Controller or XenApp server to capture key data points and CDF traces, then securely upload the package to Citrix Technical Support.
- Citrix UPS Print Driver Certification Tool: tests a driver's compatibility with the Universal Print Server.
- StressPrinters: stress-test print drivers when unsure.
- XenApp Printer Driver Manager (Feb 2012, XenApp 6.5): manage XenApp print drivers and update the Automatic Printer Replication List via GUI.
- Citrix Printing Tool 3.1: configure/troubleshoot the Citrix printing subsystem.
- CtxAdmTools: a collection of Citrix troubleshooting/diagnostic tools.

Also, XenApp/XenDesktop 7.6 FP3 added an Always-On logging feature for the print server and printing subsystem on the VDA; use the Start-TelemetryUpload PowerShell cmdlet to zip logs for email or upload to Citrix Insight Services.

## Verwante notities

- [Bas's checklist to speed up and clean up Citrix printing](bas-citrix-printing-optimization-checklist.md)
- [Citrix Insight Services: automated log analysis and health checks](citrix-insight-services.md)
- [Citrix Print Management Service](citrix-print-management-service.md)
- [Citrix printing troubleshooting and verification tools](citrix-printing-troubleshooting-tools.md)
- [Citrix Scout: the aggregating troubleshooting tool](citrix-scout-aggregator.md)
- [Citrix Diagnostic Toolkit and Supportability Pack collections](citrix-toolset-collections.md)
- [Bas's print driver best practices](print-driver-best-practices.md)
- [Print-related troubleshooting tools (Print Detective, UPS Cert Tool, StressPrinters)](print-troubleshooting-tools.md)
