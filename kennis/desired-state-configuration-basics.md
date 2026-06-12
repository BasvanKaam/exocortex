---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-10
tags: [powershell, dsc, automation, configuration-management]
layer: reference
gedateerd: nee
bron: basvankaam-blog
---

# How PowerShell DSC works: authoring, MOF, push and pull

Desired State Configuration is a PowerShell management platform for declaring and maintaining a desired state across one or many machines: software install/config, files and folders, registry, local users and groups, server roles, and more. If state drifts, DSC corrects it back to the declared state.

The model has two phases:

- Authoring phase: write a PowerShell configuration script; executing it builds the configuration in memory and compiles it into a MOF file (Managed Object Format) that holds the actual desired state. MOF files can also be produced other ways (third-party tooling, a plain text editor); PowerShell just adds declarative syntax and IntelliSense.
- Deployment phase: the MOF is applied to target machines. Re-applying only changes settings that don't match the MOF; matching settings are skipped. Two delivery methods: push (most common, via Start-DscConfiguration) and pull (set up an HTTP/HTTPS web server or SMB file server for nodes to pull from).

DSC is agentless, free, flexible, works on-prem and in cloud, and ships with resource providers (modules) so you don't start from scratch; extra sets are released as 'waves', and you can author custom resource providers.

*Bron: blogpost 'Desired State Configuration & the Citrix XenDesktop DSC Tech Preview' (2015-04-07), basvankaam.com.*

## Verwante notities

- [DSC prerequisites: WMF / PowerShell 4.0 on every machine involved](dsc-prerequisites-wmf4.md)
- [Infrastructure as Code (IaC) and Its Benefits](infrastructure-as-code-basics.md)
- [Learn the database back-end, not just the front-end](learn-the-database-back-end-not-just-the-front-end.md)
- [Prefer PowerShell over the GUI for Citrix FMA work](powershell-over-gui-for-citrix.md)
- [Citrix's XenDesktop DSC Tech Preview is one to watch](stance-dsc-worth-watching.md)
- [Everything you do in Studio is PowerShell underneath](studio-is-powershell-underneath.md)
