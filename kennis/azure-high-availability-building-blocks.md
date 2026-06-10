---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-09
tags: [high-availability, availability-zone, availability-set, fault-domain, region]
layer: reference
bron: van-de-basis-tot-meester-in-de-cloud
---

# Azure high-availability building blocks

The cloud architecture offers ways to make VMs, data and services highly available with little effort - often just ticking the right checkboxes while the provider handles the rest. Key components:
- Region: a geographic location (hundreds of km apart) where generally multiple datacenters are built. Spreading across regions protects against large disruptions or natural disasters that can hit a whole region; if a region fails, a (possible) failover to another region occurs.
- Availability Zone: effectively a datacenter (tens to hundreds of km apart). Most regions contain 2 or more datacenters/zones. Spreading resources across zones in the same region substantially raises availability so one datacenter's failure doesn't take down everything - e.g. keeping at least 50%+ of users productive.
- Availability Set: a group of VMs arranged together to raise availability; protects against local VM-level failures within one zone by spreading VMs across hardware layers. Note: you cannot use Availability Sets and Zones together - it's one or the other, and the logical choice is usually a Zone because it offers higher protection.
- Fault and Update Domains: both Sets and Zones use these to further minimise downtime. Fault Domains run VMs on separate racks and physical hardware so a hardware fault doesn't hit all VMs in the set. Update Domains split VMs into separate logical groups for software updates, so planned maintenance doesn't hit all VMs at once.

Combining these creates a robust, highly available environment resilient to both local failures and larger region-specific incidents - the infrastructure is already there.

## Bron-citaten (NL, verbatim)

> De infrastructuur is er al, het is vaak een kwestie van de juiste checkboxen aanvinken, de Cloudprovider regelt de rest.

## Verwante notities

- [Autoscaling and the Black Friday Scenario](autoscaling-black-friday-scenario.md)
- [The Azure cloud hierarchy: tenant down to resources](azure-cloud-hierarchy.md)
- [Cloud providers build their own servers and hypervisors](cloud-providers-build-own-servers-hypervisor.md)
- [Standard components of a disaster recovery (DR) plan](disaster-recovery-plan-components.md)
- [Global cloud scale: regions, zones, and which continent has no datacenters](global-scale-regions-zones-datacenters.md)
- [Why high availability and DR matter: ransomware and data hostage](ransomware-data-hostage.md)
- [Technical/Functional Design as Cloud Blueprint](technical-functional-design-blueprint.md)
