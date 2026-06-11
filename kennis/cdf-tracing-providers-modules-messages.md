---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, cdf, cdf-control, citrix-scout, tracing, troubleshooting]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# How CDF tracing works: providers, modules, trace messages

How it worked then (XenDesktop 7.x era): CDF stands for Citrix Diagnostics Facility. Every Citrix component (e.g. a Delivery Controller) is split into trace providers a.k.a. categories (USB, ICA traffic, printing, FMA services, profile management, provisioning, etc.). Each category is divided into modules, and each module consists of trace messages.

When a CDF trace runs (via Scout or CDF Control), diagnostic info is collected by reading the trace messages from the modules; a trace message responds with its current state, which could be an error code. A Delivery Controller holds far more modules/trace messages than a VDI desktop VM. Scout scans and reads all modules by design (simple), using PowerShell in the background to detect them; CDF Control lets you select/deselect individual modules. This trace-provider concept is not Citrix-specific - other vendors apply the same technique.

*Bron: blogpost 'Troubleshooting the XenDesktop FMA - Citrix Scout deep dive, part one' (2015-03-17), basvankaam.com.*

## Verwante notities

- [CDF Control, trace providers, and TMF file parsing](cdf-control-and-tmf-files.md)
- [The Citrix XenDesktop/XenApp 7.x troubleshooting toolset](citrix-7x-troubleshooting-toolset.md)
- [Citrix Call Home telemetry and how it worked](citrix-call-home-telemetry.md)
- [Scout 3.0 swapped CDF-Control for Logman.exe (ETW)](citrix-scout-3-cdfcontrol-to-logman.md)
- [Citrix Scout, TaaS and Insight Services as the 2015 troubleshooting chain](citrix-scout-taas-insight-services.md)
- [Parsing CDF traces: .etl files, TMF files, public vs private](etl-parsing-tmf-files-public-private.md)
- [The PortICA service (PicaSvc2.exe) and why it's excluded from default traces](portica-picasvc2-ica-service-role.md)
