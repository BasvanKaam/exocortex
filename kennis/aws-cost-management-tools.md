---
type: kennis
merk: bvk
domein: financieel
status: actief
datum: 2026-06-09
tags: [aws, cost-management, reserved-instances, spot-instances, reference]
layer: reference
bron: van-de-basis-tot-meester-in-de-cloud
---

# AWS cost management and optimisation tools

Reference list of Amazon Web Services cost-management and optimisation tooling cited by Bas.

**Analysis & monitoring**: AWS Cost Explorer (cost and trends per service/account); AWS Budgets; AWS Trusted Advisor (savings advice, e.g. shutting unused instances); AWS Compute Optimizer (right instance type/size); AWS Cost Anomaly Detection (proactive alerts on unexpected cost rises).

**Reduction & optimisation**: tagging strategy (e.g. Project=Marketing, Owner=JohnDoe); AWS Organizations & Linked Accounts; Reserved Instances (RIs) and Savings Plans (save up to 75% on EC2 and RDS by committing capacity); Spot Instances (much lower cost for temporary workloads); AWS Instance Scheduler (automate on/off of unused EC2); S3 Intelligent-Tiering (auto-move data to cheaper storage classes).

**Budgeting & automation**: Auto-scaling and Elastic Load Balancing; Lambda Scheduling (serverless on/off outside hours); CloudFormation cost controls; AWS Cost Categories; AWS Savings Plans (save up to 72% on compute and database costs).
