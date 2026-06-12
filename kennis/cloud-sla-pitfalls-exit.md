---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-09
tags: [sla, cloud-exit, compensation, uptime, service-credit]
layer: rich
bron: van-de-basis-tot-meester-in-de-cloud
---

# SLA pitfalls to analyse for a cloud exit strategy

Bas urges understanding and analysing the provider's Service Level Agreements as part of an exit strategy. While the basic SLA structure is often the same, each service (storage, compute, networking, etc.) has specific descriptions of expected availability. His specific warnings:

- SLA breaches are only acknowledged if the customer reports them in time - so set clear monitoring and reporting procedures to react promptly and claim the compensation laid down in the SLA.
- Providers often use phrasing like 'including, but not limited to', meaning the information you must supply for a claim may not be fully clear and extra data is needed.
- Many SLAs state the provider will make 'commercially reasonable efforts to process claims during the following month and within forty-five (45) days of receipt' - so the compensation timeline is not always guaranteed.
- SLAs usually state that a 'service credit is the sole remedy' for performance and availability issues - no further legal action or other compensation can be demanded, and the credit is typically capped at the monthly cost of that service in the billing month. This is critical if the organisation depends on high availability of several crucial services.
- SLAs define terms like available minutes, uptime and downtime; planned maintenance windows are often excluded from uptime calculations, so real availability can be lower than first expected.

SLA Extra notes: resources must meet certain conditions; don't forget supporting documentation; self-caused or planned downtime doesn't count; SLAs may be changed without notice; beta services often fall outside an SLA; and it concerns the SLA on a monthly basis. He adds it is worth studying SLAs in earlier cloud-adoption phases too, not just for an exit.

## Bron-citaten (NL, verbatim)

> “Never get so busy with the Cloud that you forget to make an exit plan.” – Dolly Parton (sort of)

## Verwante notities

- [Key Takeaways - cloud exit strategy (Chapter 12)](cloud-exit-key-takeaways.md)
- [Bas's checklist of points of attention for a cloud exit](cloud-exit-points-of-attention.md)
- [Cloud exit strategy: why and how](cloud-exit-strategy.md)
- [A cloud exit strategy is insurance you hope not to need](cloud-exit-strategy-as-insurance.md)
- [The six-step process for building a cloud exit strategy](cloud-exit-strategy-steps.md)
- [Standard components of a disaster recovery (DR) plan](disaster-recovery-plan-components.md)
- [Opdracht 10: Exit Strategy (XYZ-Care)](exit-strategy-assignment-xyz-care.md)
- [ITIL Service Management in Cloud Environments](itil-in-cloud-environments.md)
- [ITIL Processes That Need Attention When Introducing Cloud](itil-process-changes-for-cloud.md)
- [Performance and Stability: You Trade Control for Provider Scale](performance-stability-and-provider-scale.md)
- [SLA availability to allowed-downtime reference (the nines)](sla-availability-nines-downtime-table.md)
