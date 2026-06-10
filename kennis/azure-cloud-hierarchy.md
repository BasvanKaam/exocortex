---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-09
tags: [azure, tenant, subscription, management-group, resource-group, vnet]
layer: reference
bron: van-de-basis-tot-meester-in-de-cloud
---

# The Azure cloud hierarchy: tenant down to resources

Bas walks through the Azure hierarchy, which organises, manages and secures cloud resources at different levels, with flexibility for small and large environments. Many of these layers can be managed independently (e.g. a cloud administrator may have no access to financial data and cannot change management-group permissions), all governed via Azure Role Based Access (RBAC).

- Azure Tenant: the fundamental building block; a unique instance of Entra ID (formerly Azure AD) tied to a specific organisation. Manages users, groups and policies. One or more subscriptions attach to a tenant. Function: managing identity and access at the organisational level.
- Azure Subscription: a container in which you manage and organise all resources (servers, storage, databases). Central to billing and cost control; can hold multiple resource groups and separate projects/cost centres. Function: scalability and structure with clear separation of budgets, costs and projects.
- Management Groups: an extra management layer for larger orgs with multiple subscriptions; group subscriptions and apply central policies/role assignments that automatically cascade to underlying subscriptions. Function: simplifying management and enforcing consistent governance at scale.
- Resource Groups: containers grouping related resources that share the same lifecycle, so you can manage, move or delete them together. Function: structuring related resources for easier lifecycle management. (Bas's aside: a created Azure resource cannot be renamed, regardless of type.)
- Virtual Networks (VNet): a logical network to connect and isolate resources; can connect to other VNets, on-premises, or the internet via VPN, ExpressRoute or peering.
- Subnets: subdivide a VNet into smaller segments for more control over traffic and per-segment security policy; closely resembles a physical network.
- Resources: the actual building blocks - VMs, storage accounts (e.g. Azure Files), databases, web apps, load balancers, key vaults, and hundreds more - placed within resource groups and, if needed, VNets/subnets.

Bas singles out the Azure Global Administrator as a role to handle carefully.

## Bron-citaten (NL, verbatim)

> Wist je trouwens dat je een aangemaakte Azure resource, ongeacht het type niet van naam kunt veranderen?

## Verwante notities

- [Azure Files: a cloud NAS, plus Azure File Sync for hybrid](azure-files-cloud-nas.md)
- [Azure high-availability building blocks](azure-high-availability-building-blocks.md)
- [Microsoft Azure Profile and Strengths](azure-profile-strengths.md)
- [Cloud providers build their own servers and hypervisors](cloud-providers-build-own-servers-hypervisor.md)
- [Global cloud scale: regions, zones, and which continent has no datacenters](global-scale-regions-zones-datacenters.md)
- [Tenant vs Account vs Project: the top-level boundary across Azure, AWS, Google](tenant-account-project-across-providers.md)
