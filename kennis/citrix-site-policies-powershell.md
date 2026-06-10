---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [site-policies, powershell, entitlement, assignment, broker]
layer: reference
bron: inside-citrix-fma
---

# Citrix Site policies: Entitlement, Assignment, Site Access

While Catalogs and Delivery Groups normally grant access to resources, PowerShell lets you get more granular via Site policies.

Entitlement policies apply to pooled and shared desktops; you can explicitly deny specific users access without creating a separate exclusion group. Two types: BrokerEntitlementPolicyRule (desktops) and BrokerAppEntitlementPolicyRule (applications).

Assignment policies do the same but apply to dedicated private desktops: BrokerAssignmentPolicyRule (desktops) and BrokerAppAssignmentPolicyRule (applications).

Entitlement gotcha: when you create a Delivery Group with delivery type Desktops and Applications, Studio creates one Desktop and one App Entitlement Policy Rule, each entitling one session, but doesn't expose the user filter, so both are available to all group users. Use `Set-BrokerEntitlementPolicyRule` to set `IncludeUserFilterEnabled` to True and add an AD security group, limiting access to just that group.

Site Access policies are about connections in general and the conditions to meet once established (client IP, protocol, Smart Access filters, hostnames), and can exclude or deny connections. When a Delivery Group is created, two access rules are added by default: one for direct connections and one for connections through NetScaler. Inspect with `Get-BrokerAccessPolicyRule -DesktopGroupName ...` and edit with `Set-BrokerAccessPolicyRule`.

## Verwante notities

- [Citrix Studio: the central management console](citrix-studio-overview.md)
- [The Delivery Controller as the heart of the FMA](delivery-controller-heart-of-fma.md)
- [External user authentication through NetScaler](external-authentication-through-netscaler.md)
- [FMA Broker Service (XML/STA) and its responsibilities](fma-broker-service.md)
- [Citrix Studio Configuration sub-nodes](studio-configuration-subnodes.md)
- [Citrix Studio console root nodes](studio-console-root-nodes.md)
