---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-09
tags: [iac, terraform, desired-state, automation, beheer-2-0]
layer: reference
bron: van-de-basis-tot-meester-in-de-cloud
---

# Infrastructure as Code (IaC) and Its Benefits

Infrastructure as Code means managing and provisioning IT infrastructure based on code rather than manual processes. You write code (e.g. in JSON, YAML, or Terraform) to define your infrastructure, and a pipeline rolls it out automatically.

Benefits the book lists:
- **No manual changes**: everything is done via code, ensuring consistency and reducing errors (vs logging into a system to make changes by hand).
- **Reproducibility**: instead of fixing problems by hand, you re-deploy the whole environment to its original state by re-running the IaC code, making rollback easier and faster.
- **Desired State Configuration**: you define the desired state in code, and tools like Terraform and Kubernetes keep reality matching that state, adjusting automatically when needed.
- **New skills and platforms**: IaC often demands new skills such as PowerShell, Python, JSON, YAML, Terraform and Kubernetes.

This modern way of managing infrastructure is also called **Beheer 2.0** ("Management 2.0"), enabling teams to deliver faster and more reliably. The catch: the learning curve is steep.

## Verwante notities

- [Bas's War Story: The IaC Dependency Trap](bas-iac-dependency-trap.md)
- [Bas: IaC Creates Dangerous Key-Person Dependency](bas-iac-key-person-risk.md)
- [Cloud Cultural Shifts: DevOps, Automation, New Roles](cloud-cultural-shifts-overview.md)
- [Cloud-Native: Designed for the Cloud from the Start](cloud-native-definition.md)
- [Citrix Lifecycle Management Services and blueprints](cwc-lifecycle-management-services.md)
- [How PowerShell DSC works: authoring, MOF, push and pull](desired-state-configuration-basics.md)
- [Bas: Saying You're Cloud-Native vs Actually Being It](saying-cloud-native-vs-being-it.md)
- [Introducing Agile and Plan-Do-Check-Act in Execution](scaf-execution-agile-pdca-intro.md)
- [WCGF Domain: Platform Design, Service and Tooling Integration](wcgf-platform-design-tooling-integration-domain.md)
