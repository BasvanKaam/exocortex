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
