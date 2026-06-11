---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [high-availability, best-practice, resilience, design]
layer: rich
bron: inside-citrix-fma
---

# Bas's 'one is none' rule for resilience

Bas's guiding redundancy maxim: your environment is only as strong as its weakest link, so apply the 'one is none' rule wherever and whenever it makes sense. A single instance of any critical component is effectively no resilience at all.

He applies it across the FMA: deploy at least two Delivery Controllers per Site (and per Zone where possible), make PVS infrastructure highly available, and pair NetScalers (the rule applies to NetScalers as well). It is a recurring design principle throughout the book rather than a one-off remark.

## Bron-citaten (NL, verbatim)

> Your environment is as strong as its weakest link. Make sure to apply the 'one is none' rule wherever and whenever it makes sense.
>
> Remember the one is none rule? Well, it applies to NetScalers as well.

## Verwante notities

- [Bas: IaC Creates Dangerous Key-Person Dependency](bas-iac-key-person-risk.md)
- [Bas's take on application-aware HA alternatives for SQL](bas-on-application-aware-ha-alternatives.md)
- [High-availability options for the Central Site database](central-site-database-ha-options.md)
- [DFS: Stand-alone vs Domain-based Namespaces](dfs-standalone-vs-domain-based.md)
- [DHCP 80/20 redundancy rule](dhcp-80-20-rule.md)
- [Standard components of a disaster recovery (DR) plan](disaster-recovery-plan-components.md)
- [FMA service high availability via peer service groups](fma-services-high-availability.md)
- [MSCS Cluster Building Blocks](mscs-cluster-building-blocks.md)
- [NetScaler high availability and clustering](netscaler-high-availability-clustering.md)
- [The 'one is none' rule and Delivery Controller high availability](one-is-none-delivery-controller-ha.md)
- [PVS high availability](pvs-high-availability.md)
- [Universal Print Server load balancing and HA (7.9)](ups-load-balancing-ha.md)
