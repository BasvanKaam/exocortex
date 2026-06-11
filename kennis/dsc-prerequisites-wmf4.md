---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-10
tags: [powershell, dsc, wmf, prerequisites]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# DSC prerequisites: WMF / PowerShell 4.0 on every machine involved

How it worked then (2015). DSC required PowerShell 4.0 / Windows Management Framework 4.0, present by default in Windows Server 2012 R2 and Windows 8.1. Windows 7 and Windows Server 2008 R2 were supported but needed additional install steps. Notably, WMF / PS 4.0 could not be installed on Windows 8. You needed to be a local Administrator, and WMF/PS 4.0 had to be on every machine in the process: the authoring/compiling machine and every target node receiving the desired state.

*Bron: blogpost 'Desired State Configuration & the Citrix XenDesktop DSC Tech Preview' (2015-04-07), basvankaam.com.*

## Verwante notities

- [How PowerShell DSC works: authoring, MOF, push and pull](desired-state-configuration-basics.md)
- [Inspecting prerequisites up front saves the whole deployment](prerequisites-discipline-saves-time.md)
