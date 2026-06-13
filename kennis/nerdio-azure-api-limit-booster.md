---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [nerdio, nme, azure, api-limits, arm, graph-api, scale]
layer: reference
gedateerd: ja
bron: nerdio-content
---

# Azure API limits and Nerdio's API Limit Booster

Both AVD and Nerdio Manager drive the underlying Azure Resource Manager (ARM) via the Graph API. Every "action" invokes an API call: starting, stopping or deallocating hosts, GUI interactions, autoscaling, collecting metrics (CPU, RAM, AVD session info), scheduled tasks, and more.

Azure imposes API call limits at both subscription and tenant level. In large AVD deployments this matters — hitting the limit means certain actions simply don't execute. Limits are scoped to the security principal (user or application) making the request and the subscription ID; some VM API limits are also scoped to a specific Azure region. So adding subscriptions, regions and security principals increases the aggregate limit, but sometimes that still isn't enough.

Nerdio's API Limit Booster lets you register additional applications in Azure AD/Entra to issue calls. Nerdio round-robins across the linked client apps during normal operations, distributing API calls across each one, growing the total by a factor of n (n = number of linked apps). In theory this lets you scale environment size effectively without bound.

*Bron: Nerdio-content 'Aankondigingen-thisismine' ((root)).*

## Verwante notities

- [Delegated vs Application Permissions (Microsoft Graph)](delegated-vs-application-permissions-graph.md)
- [Active/Active DR for AVD Across Two Regions](nerdio-active-active-dr.md)
- [Nerdio autoscaling engine: pooled hostpool scaling logic](nerdio-autoscaling-engine-pooled-hostpools.md)
- [Permissions to Install and Operate Nerdio (NME)](nerdio-install-and-linking-permissions.md)
