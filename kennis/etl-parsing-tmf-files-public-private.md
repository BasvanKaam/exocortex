---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, cdf-control, tmf, etl, parsing, troubleshooting]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Parsing CDF traces: .etl files, TMF files, public vs private

How it worked then: CDF traces are saved as .etl files (under AppData\Local\Temp\Scout\ of the user running the trace - NOT the C:\XDLogs\ folder, which is only used by Collect & Upload). Raw .etl content is partly GUIDs and unreadable, so it must be parsed.

Parsing needs (1) a tool that can parse (CDF Control or CDF Monitor in the Citrix world) and (2) TMF (Trace Message Format) files - structured text files holding the instructions for parsing/formatting the binary trace messages. TMF is a general (WPP/WDK) concept, not a Citrix invention. Two flavours: public TMF files (for self-service parsing, downloadable via CDF Control) and private TMF files (CTX Support eyes only - needed to expose certain issues, requiring a support contract). Advice: always download TMF files locally rather than relying on the online TMF server, which can be slow on large traces or go offline.

*Bron: blogpost 'Troubleshooting the XenDesktop FMA - Citrix Scout deep dive, part one' (2015-03-17), basvankaam.com.*

## Verwante notities

- [CDF Control, trace providers, and TMF file parsing](cdf-control-and-tmf-files.md)
- [How CDF tracing works: providers, modules, trace messages](cdf-tracing-providers-modules-messages.md)
- [The Citrix XenDesktop/XenApp 7.x troubleshooting toolset](citrix-7x-troubleshooting-toolset.md)
- [Scout 3.0 swapped CDF-Control for Logman.exe (ETW)](citrix-scout-3-cdfcontrol-to-logman.md)
- [Citrix Scout: the aggregating troubleshooting tool](citrix-scout-aggregator.md)
- [Run a CDF trace before you contact Citrix Support](trace-before-you-call-citrix-support.md)
