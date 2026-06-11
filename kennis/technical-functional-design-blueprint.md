---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-09
tags: [design, technical-design, hld, lld, scaf]
layer: rich
bron: van-de-basis-tot-meester-in-de-cloud
---

# Technical/Functional Design as Cloud Blueprint

Before building Cloud infrastructure, Bas insists on first drawing up a detailed technical/functional design that acts as a blueprint, helping build the environment in a structured way. It is a document capturing all technical and functional details: how the infrastructure is/will be built, which components are needed and how everything works together. It serves as a practical tool for communication and planning so all stakeholders share a clear picture.

Technical design content (examples): Compute (VMs, containers, CPU/RAM specs), Network (architecture, segments, subnets, VPNs, on-prem links, load-balancers, firewall rules), Storage (block/file/object, performance, scalability, security), Security (identity management, encryption, protocols, access monitoring), Identity & Access (IAM, MFA, authorization), Continuity & Disaster Recovery (back-ups, replication, failover), and Automation (Infrastructure as Code, auto-scaling, monitoring/alerting).

Why bother: it gets everyone's noses pointing the same way ('alle neuzen dezelfde kant op'), provides structure, prevents misunderstandings, and avoids errors or extra costs during the build. It is some work but worth it, and a reusable template for the future. Note: a distinction is usually made between High Level Design (HLD) and Low Level Design (LLD), i.e. less versus more detail.

## Verwante notities

- [Acceptance Criteria Checklist for System Delivery](acceptance-criteria-checklist.md)
- [Azure high-availability building blocks](azure-high-availability-building-blocks.md)
- [DaaS / VDI Additions to the Technical Design](daas-vdi-technical-design-considerations.md)
- [Enterprise Architecture (EA) and TOGAF](enterprise-architecture-togaf.md)
- [Functional Design with Functional Tests](functional-design-and-functional-tests.md)
- [Opdracht 9: Migration Mastery - Strategy to Execution (XYZ-Care)](migration-mastery-assignment-xyz-care.md)
- [SCAF Documentation and Templates](scaf-documentation-templates.md)
- [SCAF Execution Phase (Uitvoeringsfase) Overview](scaf-execution-phase-overview.md)
- [SCAF Execution Phase Supporting Documentation](scaf-execution-supporting-documentation.md)
