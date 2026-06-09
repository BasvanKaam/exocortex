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
