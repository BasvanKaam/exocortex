---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [idee, addie, instructional-design, api, training-method, l-and-d]
layer: reference
gedateerd: nee
bron: nerdio-training
---

# Instructional Method: Teaching an API by Scope Boundary, Not by Coding

Bas's design pattern for an API training that deliberately does not teach production coding. The reusable moves:

- **Open with an explicit scope boundary** to kill ambiguity around an overloaded word. The product uses many internal APIs (e.g. communication with Azure services); the course covers only the documented, supported REST/Partner API exposed for external use. He writes in-scope and out-of-scope lists side by side so expectations are set and confusion is avoided.
  - In scope: the public REST API, official docs and supported tooling (Swagger/OpenAPI, Postman), getting-started and manual-config guidance, auth/permission concepts, capabilities/limitations/governance/deprecations.
  - Out of scope: internal Azure communication, backend architecture, reverse-engineered/undocumented endpoints, coding tutorials/full scripts/SDKs/CI-CD pipelines.
- **Teach documentation literacy as the core skill**: locate and interpret official docs, read Swagger/OpenAPI endpoint definitions and schemas, and use Postman as a documentation-driven validation tool, focus on interpretation rather than execution.
- **Treat permissions as a functional variable**: a whole part on how permissions affect available functionality and how to diagnose permission-related failures using the documentation.
- **Position the PowerShell module as a consumption layer / wrapper** over the REST API, not a separate thing to master.
- **End with governance**: deprecated endpoints/properties, tracking API changes, responsible long-term usage.

The takeaway method: when the goal is comprehension and safe use rather than building, lead with a hard scope boundary and make 'read the official docs/Swagger' the central competency. Reusable for any tool-understanding (vs tool-building) course.

*Bron: Nerdio-content 'ADDIE - REST API for Nerdio Manager for Enterprise' (Training).*

## Verwante notities

- [Delegated vs Application Permissions (Microsoft Graph)](delegated-vs-application-permissions-graph.md)
- [How Bas reviews Nerdio L&D content as SME](nme-course-content-review-method.md)
- [Training content must be technically true and honestly named](training-must-be-technically-true.md)
- [Why Windows 365 enablement needs Global Admin (org consent)](windows-365-enablement-permissions.md)
