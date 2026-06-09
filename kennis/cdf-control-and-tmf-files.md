---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [cdf, diagnostics, tmf, etl, tracing]
layer: reference
bron: inside-citrix-fma
---

# CDF Control, trace providers, and TMF file parsing

CDF stands for Citrix Diagnostic Facility. CDF Control is an event tracing controller/consumer that captures CDF trace messages from various Citrix tracing providers. It has been around for over eight years and is still one of the most-used diagnostic tool kits. It is built into Scout and available as a standalone download (CTX111961); local admin permissions are required to start tracing. Good practice is to collect CDF traces before opening a Citrix support case.

Each Citrix component is split into categories (trace providers) such as USB, ICA traffic, printing, FMA services, profile management, and provisioning services. Categories are divided into modules, which consist of trace messages. A running trace reads the trace messages, which respond with their current state (possibly an error code). A Delivery Controller holds far more modules/trace messages than a VDI VM.

CDF traces are saved with the .etl extension under `AppData\Local\Temp\Scout\`. Because logged data is partly in GUID form, .etl files must be parsed with TMF (Trace Message Format) files before being readable. TMF files come in public (for personal parsing) and private (CTX Support only) variants. Public TMF files can be downloaded via CDF Control or used live from an online TMF server; Bas advises always downloading them, because online parsing fails on high-latency lines, offline TMF servers, or large traces. Parsing .etl files is relatively easy, but reading them to find the actual fault requires special skills.
