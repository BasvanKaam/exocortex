---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-11
tags: [sla, availability, uptime, reference, cloud-masterclass]
layer: reference
gedateerd: nee
bron: salomon-masterclass
---

# SLA availability to allowed-downtime reference (the nines)

Reference table Bas uses to make abstract SLA percentages concrete by translating them into allowed downtime per year, month, and week.

| Availability | Down/year | Down/month | Down/week |
|---|---|---|---|
| 90% (one nine) | 36.5 days | 72 h | 16.8 h |
| 95% | 18.25 days | 36 h | 8.4 h |
| 99% (two nines) | 3.65 days | 7.2 h | 1.68 h |
| 99.9% (three nines) | 8.76 h | 43.2 min | 10.1 min |
| 99.99% (four nines) | 52.56 min | 4.32 min | 1.01 min |
| 99.999% (five nines) | 5.26 min | 25.9 s | 6.05 s |
| 99.9999% (six nines) | 31.5 s | 2.59 s | ~0.6 s |

Teaching point: each added nine cuts allowed downtime by roughly an order of magnitude, and the cost of guaranteeing it rises steeply. Use when reading or negotiating a vendor SLA so the percentage maps to real outage minutes.

*Bron: Salomon-IT 'SLA uptime percentages'.*

## Verwante notities

- [A cloud exit strategy is insurance you hope not to need](cloud-exit-strategy-as-insurance.md)
- [SLA pitfalls to analyse for a cloud exit strategy](cloud-sla-pitfalls-exit.md)
- [Compliance and risk as operational governance](compliance-risk-operational-governance.md)
- [Design for Restore, Not Backup (RPO/RTO/MTPD First)](design-for-restore-not-backup.md)
- [Curated cloud self-study resources (Masterclass handout)](masterclass-curated-cloud-learning-resources.md)
- [KPIs in the SCAF Adoption phase: making success measurable](scaf-kpis-in-adoption-phase.md)
