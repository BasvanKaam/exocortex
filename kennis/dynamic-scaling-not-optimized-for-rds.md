---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [rds, azure, autoscale, wvd]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Azure Dynamic Scaling was not RDS-aware (2019)

How it worked then: Azure Dynamic Scaling could increase or decrease VM count manually or on metrics, but it was not optimized for RDS workloads. New machines were not automatically added to the RDS host session collection, nor removed, you did that manually. When scaling down you also had to drain session hosts of active user sessions before shutting them down. WVD differed because brokering, load balancing and so on were built in 'as a service', so the manual session-collection juggling did not apply to WVD itself.

*Bron: blogpost 'Combine WVD, IaaS RDS, on-prem RDS to scale, protect & migrate' (2019-04-29), basvankaam.com.*

## Verwante notities

- [Microsoft's WVD power scripts are not real autoscaling](nerdio-vs-microsoft-power-management-scripts.md)
