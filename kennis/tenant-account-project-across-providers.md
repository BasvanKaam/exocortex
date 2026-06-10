---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-09
tags: [tenant, aws-account, gcp-project, iam, entra-id]
layer: reference
bron: van-de-basis-tot-meester-in-de-cloud
---

# Tenant vs Account vs Project: the top-level boundary across Azure, AWS, Google

All three big providers use a comparable approach to the isolated top-level workspace, but naming differs:
- Microsoft Azure - the tenant: the foundation in which an organisation's services and resources are built and managed; a shielded environment, assigned to you when you start with Azure. Here you handle identity and access: central management of users/roles/rights, security and organisation of resources, and coupling with Azure Active Directory (now Entra ID) to authenticate and authorise users.
- AWS - your own account: a shielded space (like a digital vault) where you manage all cloud services and data. Everything you create stays within your account; access is managed with IAM (Identity and Access Management); AWS Organizations lets you create and centrally manage multiple accounts.
- Google Cloud - projects as workspaces: everything begins with a project, a demarcated workspace; user rights are set with IAM; a Google Cloud Organization lets you manage multiple projects from one central point.

## Verwante notities

- [AWS Profile and Strengths](aws-profile-strengths.md)
- [The Azure cloud hierarchy: tenant down to resources](azure-cloud-hierarchy.md)
- [Microsoft Azure Profile and Strengths](azure-profile-strengths.md)
- [No real standards across cloud providers; identical services, different names](cloud-providers-no-standards-naming.md)
- [Google Cloud Platform Profile and Strengths](gcp-profile-strengths.md)
- [The Big Three Cloud Providers (AWS, Azure, GCP)](the-big-three-cloud-providers.md)
