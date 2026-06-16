---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-10
tags: [cloud, latency, ping, aws-azure-gcp, benchmarking]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# A simple DIY method to compare Cloud datacenter latency

His method (2019) to give an indication of latency to European datacenters across AWS, Azure and Google: spin up one VM on each platform from a standard marketplace Windows Server 2016 Datacenter template, basic HDD, a few GB RAM, single vCPU, default network config, reachable over RDP/Ping. Ping each for at least 5 straight minutes independently and record the average. He ran two tests: standard ICMP, and an HTTP-request based test via the community tool pingtestlive.com (which uses HTTP response status codes to approximate round-trip time). All tests were run from one fixed location (IJmuiden, NL) over a stable cable connection, against European regions only since testing the whole globe from one spot makes no sense.

How it did it then. He explicitly framed it as indicative only: 'do your own research before you commit to anything.'

*Bron: blogpost 'Version 2.0 of the Cloud Services Cheat Sheet is now live' (2019-02-06), basvankaam.com.*

## Verwante notities

- [Durable barriers to public cloud adoption](barriers-to-public-cloud-adoption-2016.md)
- [Bas's Cloud 'Cheat Sheets' mapping provider service names](bas-cloud-cheat-sheets.md)
- [Physical and performance limits of working from the cloud](cloud-physical-and-performance-limits.md)
- [Same cloud service, different name per vendor](cloud-service-naming-differs-per-vendor.md)
- [Global cloud scale: regions, zones, and which continent has no datacenters](global-scale-regions-zones-datacenters.md)
- [Hybrid Latency and the Region-Choice Pitfall](hybrid-latency-region-choice-pitfall.md)
- [Indicative cost overview: split the totals, show the assumptions, never call it a quote](indicative-cost-overview-method-assumptions-and-reserved-instances.md)
- [Bas's warning: Cloud apps with on-premises backends invite latency trouble](latency-cloud-app-onprem-backend.md)
- [Comparing a Physical Server to Cloud Isn't Fair](physical-vs-cloud-server-not-fair-comparison.md)
