---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [citrix, call-home, telemetry, scout, insight-services, xenapp, xendesktop]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Citrix Call Home telemetry and how it worked

How it worked in 2016 (XenApp/XenDesktop 7.9, where Call Home came out of Tech Preview with auto-uploads):

- Call Home runs as a background service, the Citrix Telemetry Service, on Delivery Controllers and VDAs. It collects diagnostic data and periodically uploads telemetry packages to Citrix Insight Services (CIS) for analysis and troubleshooting.
- It collects a subset of CDF traces, registry entries from XA/XD installs, WMI info on Citrix products, a list of running processes, and any crash dumps. Much of this overlaps with what Citrix Scout could do manually via Collect & Upload.
- Traces run in memory to reduce additional IOPS on the source machine.
- Configuration data is gathered weekly; performance and usage data hourly. Default auto-upload is once a week on Sunday over HTTPS. Trace packages are compressed, max ~20 MB. Once sent, data is deleted from the local system.
- Also referred to as AOT, Always-On Tracing. Its CDF trace functionality automatically traces VDA registration plus a subset of application and desktop launches. This mattered because VDA registration issues were in the top 5 of Citrix Support cases almost every year.
- Participation requires signing in to CIS with MyCitrix credentials; credentials are not stored locally. Data is not fully anonymous, Citrix can identify the customer, the same as uploading at support's request.
- Manual collection and upload is also possible via PowerShell (using the same telemetry service), with the option to save locally first. When working with master images you had to enable Call Home scheduled updates via PowerShell. CIS could be reached directly from within Director.

*Bron: blogpost 'Citrix Call Home, the telemetry tool meant to phase out Scout' (2016-10-18), basvankaam.com.*

## Verwante notities

- [Call Home will phase out Scout, but not soon](call-home-vs-scout-prediction.md)
- [How CDF tracing works: providers, modules, trace messages](cdf-tracing-providers-modules-messages.md)
- [Citrix support model shift to Customer Success Services](citrix-customer-success-services-2017.md)
- [Scout 3.0 swapped CDF-Control for Logman.exe (ETW)](citrix-scout-3-cdfcontrol-to-logman.md)
- [Citrix Scout, TaaS and Insight Services as the 2015 troubleshooting chain](citrix-scout-taas-insight-services.md)
- [Citrix Smart Check: proactive Site health checks (agent or agentless)](citrix-smart-check-health-checks.md)
- [Citrix's serial renaming: TaaS to Insight Services to Smart Check](citrix-taas-insight-smartcheck-naming-history.md)
- [Smart Check as the future single Citrix diagnostics tool](smart-check-absorbing-cis-stance.md)
