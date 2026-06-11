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
