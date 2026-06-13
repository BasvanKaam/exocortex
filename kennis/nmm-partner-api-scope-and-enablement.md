---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [nerdio, nmm, msp, api, partner-api, swagger]
layer: reference
gedateerd: ja
bron: nerdio-training
---

# NMM Partner API: Scope and Enablement Essentials

The NMM-specific facts worth keeping (the instructional method is shared with the NME REST API doc, see that note):

- The MSP product's external interface is called the **Partner API** (a.k.a. the REST API for the MSP product). It lets MSPs automate actions available in the NMM portal via REST, such as managing host pools, session hosts, and desktop images.
- **Enablement path**: Settings > Integrations > REST API at the MSP level; from there you navigate to Swagger.
- Supported tooling is **Swagger** (used for documentation-driven test calls); the NME course additionally references Postman.
- A **Distributor API** exists and is explicitly out of scope unless covered in a separate course, a distinction worth noting for MSP/distributor hierarchies.
- Out of scope (same governance line as NME): internal service-to-service communication, undocumented/reverse-engineered endpoints, and full coding/SDK/CI-CD builds.

Version-specific; recheck the enablement path and capability areas against the current NMM release and release notes.

*Bron: Nerdio-content 'ADDIE - REST API for Nerdio Manager for MSP' (Training).*

## Verwante notities

- [Permissions to Install and Operate Nerdio (NME)](nerdio-install-and-linking-permissions.md)
