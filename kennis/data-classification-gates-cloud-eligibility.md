---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-11
tags: [data-classification, information-security, cloud-eligibility, ciso, public-sector, assessment-gate]
layer: reference
gedateerd: nee
bron: salomon-opdrachten
---

# Gate cloud eligibility on data classification, with CISO sign-off

In a public-sector cloud engagement (a shared-service collaboration of municipalities), Bas applies an explicit gate before the financial or functional discussion even starts: whether information may go to the cloud at all is decided first by its security classification, not by its cost or convenience. The classification, not the business case, sets the boundary; the business case operates inside that boundary.

The pattern, generalised:
- Classify each information set into a small, ordered set of tiers (here: Public, Internal, Confidential, Secret).
- Map each tier to a cloud-eligibility rule, for example:
  - **Public** - cloud allowed.
  - **Internal / Confidential** - cloud allowed *provided* it conforms to the security policy, or an explicitly accepted deviation.
  - **Secret** - no, *unless* extra measures around security, auditing and control are taken.
- Two non-negotiable principles hold regardless of tier: all information processed in the cloud service stays the responsibility of the organisation, and it may only be processed for the purposes the organisation defines.
- The **CISO (security officer) must sign off** on the measures taken where needed; the classification work is done together with the information-security working group, not by the cloud consultant alone.

Why Bas works this way:
- It makes the security conversation a **precondition** rather than an afterthought, which fits his stance that security and governance are not optional add-ons.
- It keeps the assessment **decision-ready**: a tiered table tells you at a glance which workloads are even candidates, so you don't waste a business case on something that can never be approved.
- It puts accountability where it belongs - the line manager approves the outsourcing, the organisation remains responsible for availability, exclusivity and integrity even when the work is outsourced.

Reusable takeaway: before scoring applications for cloud on cost or fit, run them through a classification gate signed off by security. The gate is cheap, it narrows the field early, and it keeps a regulated client defensible.

*Bron: geanonimiseerde aanpak uit een Salomon-IT klantopdracht (a shared-service IT collaboration of Dutch municipalities).*

## Verwante notities

- [AVG security: organizational and technical measures](avg-security-organizational-and-technical-measures.md)
- [The CCoE's role in AVG compliance and governance](ccoe-role-in-avg-compliance.md)
- [Cloud-migration suitability checklist for client/server applications](cloud-migration-suitability-checklist-client-server-apps.md)
- [Cloud Placement Decisions: the application lifecycle quadrant](cloud-placement-decisions-quadrant.md)
- [COPAFIJTL weighing matrix for a per-application cloud go/no-go](copafijtl-cloud-go-nogo-weighing-matrix.md)
