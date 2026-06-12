---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-11
tags: [cloud, cloud-native, wvd, control-plane, licensing]
layer: reference
gedateerd: ja
bron: cgit-blog
---

# Cloud-Native Control Plane Changes the Delivery Economics (WVD as Exemplar)

Bas's clarification of what 'cloud-native' means for app/desktop delivery solutions: he is talking specifically about the backend, the management/control plane, not the workload. You still run virtual machines, certainly; what is completely different is how those VMs are driven, maintained and monitored.

Cloud-native workloads are distributed (loosely coupled), built on continuous integration and delivery, not machine- or OS-dependent (operating at a higher abstraction level), API-driven, made of lightweight code and therefore extremely scalable. In other words: not monolithic, flexible, fast to change and test, based on microservices, containers, serverless and/or infrastructure as code. Put bluntly, 'no IaaS'.

Why it matters: a cloud-native control plane translates into speed and efficiency, including financially. Windows Virtual Desktop is his prime example. The apps and desktops still run on VMs, but the entire backend (the WVD management plane, the actual service you consume) is built cloud-native. Because the underlying physical and virtual resources are used far more efficiently, Microsoft can offer a single license with no minimum, since no full IaaS base infrastructure is required.

*Bron: Salomon-IT '5 (Cloud) alternatieven voor het aanbieden van je applicaties en desktops - deel 1' (CGIT Blogs).*

## Verwante notities

- [Workspace Cloud lacked an on-prem control plane in 2015](citrix-workspace-cloud-control-plane-2015.md)
- [Cloud-Native: Designed for the Cloud from the Start](cloud-native-definition.md)
- [What 'cloud native' actually means](cloud-native-workload-definition.md)
- [Early WVD architecture: Microsoft-managed PaaS control plane + reverse connect](early-wvd-architecture-control-plane.md)
- [Lift-and-shift vs cloud-native: where cloud value actually lives](lift-and-shift-vs-cloud-native.md)
- [From RDMI to Windows 10 multi-user: how WVD came to be](wvd-history-rdmi-to-windows-10-multi-user.md)
