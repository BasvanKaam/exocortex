---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-10
tags: [aws, cost-management, budgets, cost-explorer, trusted-advisor, finops]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# AWS native cost-management toolset (TCO, Budgets, Cost Explorer, Trusted Advisor)

The standard AWS-built tools Bas recommends starting with (2019): the TCO Calculator (compare traditional hosting vs AWS, with exec-ready reports), AWS Budgets (cost/usage/RI-utilization/RI-coverage budgets, notification-only, no automated actions, ~$0.02 per budget per day), Cost Explorer (track costs/usage/trends, view up to 13 months back, forecast ~3 months ahead, RI purchase recommendations), Trusted Advisor (real-time best-practice guidance on cost/performance/security), Consolidated Billing (combine usage across org accounts for volume and RI discounts), the Well-Architected Tool, and CloudWatch billing alarms plus automated actions. Durable idea: lean on the platform's own visibility and alerting tooling before reaching for third parties.

*Bron: blogpost 'THIRTY AWS Pro TIPS on how to use the Cloud more efficiently and save some money' (2019-01-16), basvankaam.com.*

## Verwante notities

- [AWS cost management and optimisation tools](aws-cost-management-tools.md)
- [Reserved, Scheduled and Spot instances as AWS cost levers](aws-instance-purchasing-models-cost.md)
- [Storage tiering and lifecycle policies cut AWS storage cost](aws-storage-tiering-and-lifecycle-cost.md)
- [Azure cost management and optimisation tools](azure-cost-management-tools.md)
- [Moving to the cloud does not automatically save money](cloud-does-not-automatically-save-money.md)
- [EC2 hibernation preserves in-memory state to save compute cost](ec2-hibernation-saves-compute-cost.md)
- [The Azure calculator is fine, but MSPs need a real one](use-vendor-calculators-not-just-azure.md)
