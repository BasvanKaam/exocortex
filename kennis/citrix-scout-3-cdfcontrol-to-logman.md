---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, scout, cdf-tracing, logman, etw, troubleshooting]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Scout 3.0 swapped CDF-Control for Logman.exe (ETW)

How it worked then (Scout 3.0, shipped with XenDesktop/XenApp 7.14, 2017): Scout's core job is still capturing CDF traces (you reproduce the issue while the trace runs), but 3.0 no longer uses CDF-Control to do it, it uses Logman.exe, which is part of Windows so nothing has to be copied to remote machines. Logman uses ETW (Event Trace Log): providers and CTL files determine what gets collected into .etl files (CDF-Control did the same). Default max sequential log size is 500 MB (chosen from years of Scout upload history). Other 3.0 changes: a deliberately simplified GUI with most collection settings removed or pushed into step-by-step flows; AoT (Always-on Tracing) collection like Call Home (subset of CDF traces for common failures e.g. VDA registration, app/desktop launches); DBDIAG and XDPing dropped (XDPing replaced by Citrix Health Assistant); no more in-GUI verbose/clear-text logging or WinRM-enable; scheduling added; Citrix Cloud credential support added; unlimited target machines (was 10); only supports 7.14+. For deep FMA-service tracing Citrix now points to the persistent PowerShell-script approach in CTX200341 (also Logman-based, logs all FMA modules by default, blacklist to exclude) rather than Scout. CDF-Control still ships as a standalone tool for advanced support cases. Dated specifics, but a good record of the CDF-Control-to-Logman/ETW transition.

*Bron: blogpost 'Citrix Scout 3.0 changes with XenDesktop/XenApp 7.14' (2017-05-22), basvankaam.com.*

## Verwante notities

- [Call Home will phase out Scout, but not soon](call-home-vs-scout-prediction.md)
- [How CDF tracing works: providers, modules, trace messages](cdf-tracing-providers-modules-messages.md)
- [Citrix Call Home telemetry and how it worked](citrix-call-home-telemetry.md)
- [Citrix Scout: the aggregating troubleshooting tool](citrix-scout-aggregator.md)
- [Citrix Scout, TaaS and Insight Services as the 2015 troubleshooting chain](citrix-scout-taas-insight-services.md)
- [Citrix's serial renaming: TaaS to Insight Services to Smart Check](citrix-taas-insight-smartcheck-naming-history.md)
- [Parsing CDF traces: .etl files, TMF files, public vs private](etl-parsing-tmf-files-public-private.md)
- [The PortICA service (PicaSvc2.exe) and why it's excluded from default traces](portica-picasvc2-ica-service-role.md)
