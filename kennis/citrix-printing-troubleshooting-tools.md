---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [printing, troubleshooting, citrix-tools, cis, perfmon]
layer: reference
bron: inside-citrix-fma
---

# Citrix printing troubleshooting and verification tools

Citrix tools useful for print (and general) troubleshooting:

- Citrix Director: real-time bandwidth used by printing.
- Print Detective: information-gathering utility for print driver problems (CTX116474).
- Citrix Scout: run from a Delivery Controller (DDC) or XenApp server to capture key data points and CDF traces, with secure upload to Citrix Technical Support (CTX130147).
- Citrix Printing Tool 3.1: configure/troubleshoot the Citrix printing subsystem (CTX122962).
- StressPrinters 1.3.2 (32/64-bit): simulate multiple sessions auto-creating printers with the same driver (CTX109374).
- UPD Finder: troubleshooting aid that calls Windows print spooler APIs to find where the Citrix UPD is installed; doesn't modify the system (CTX141351).
- UPS Print Driver Certification Tool: test a driver's compatibility with the UPS (CTX142119).
- Citrix Smart Check: proactively verify environment health and missing patches.
- Crash Detection Feature (as of 7.11): fully automates crash detection, crash dump generation, and safe automatic upload of dumps to the customer's Citrix Insight Services (CIS) account.
- PerfMon: evaluate the printing subsystem health for UPS and/or VDA via performance counters for client and network print devices.
- Event Viewer: Bas says do NOT forget this one; probably the best place to start.
- Citrix Health Assistant: focuses on VDA registration issues (XenDesktop and XenApp), running automated health checks; GUI and command-line based (CTX207624).

Note: Always-On logging for the print server and VDA printing subsystem can collate logs as a ZIP or auto-upload to Citrix Insight Services via the Start-TelemetryUpload PowerShell cmdlet. Bas expects CIS to be slowly phased out in favour of Citrix Smart Check (his educated guess).

## Verwante notities

- [Citrix Director: monitoring and troubleshooting tool](citrix-director-overview.md)
- [Citrix Insight Services: automated log analysis and health checks](citrix-insight-services.md)
- [Citrix print troubleshooting tools](citrix-print-troubleshooting-tools.md)
- [Citrix printing barely changed across 2018 releases](citrix-printing-stagnation-2018.md)
- [Citrix Scout: the aggregating troubleshooting tool](citrix-scout-aggregator.md)
- [Citrix Diagnostic Toolkit and Supportability Pack collections](citrix-toolset-collections.md)
- [Print-related troubleshooting tools (Print Detective, UPS Cert Tool, StressPrinters)](print-troubleshooting-tools.md)
- [Troubleshooting the VDA registration process and Citrix Health Assistant](vda-registration-troubleshooting.md)
