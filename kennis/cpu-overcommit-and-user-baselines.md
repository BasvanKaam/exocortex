---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [sizing, overcommit, vcpu, user-profiles, xenapp]
layer: rich
bron: inside-citrix-fma
---

# Bas on CPU over-commit and user baselines (light/medium/heavy)

Bas deliberately refuses to give a blanket rule like 'never over-commit physical CPU/core beyond 3:1 or 4:1' or 'always configure 4-8 vCPUs for a virtual XenApp server', because it makes little sense without background. First answer: what workload type(s) and characteristics (CPU/GPU/RAM intensive)? How many users per machine? Which OS? What about antivirus and monitoring software (both impact density/performance)? What hardware?

Over the years, performance baselines (per hardware/software profile) have categorised users as lightweight, medium, or heavy, advising on users per CPU/core, RAM, and (steady state) IOPS per user. The medium user is by far the most popular - a typical office worker using Office, Acrobat Reader, one or two browsers with multiple tabs, Outlook/Gmail, and the occasional YouTube clip.

With such user info, Bas concedes you do have to start somewhere: e.g. 8 vCPUs and 16/32 GB RAM on a Server 2012 R2 virtual XenApp server might not be a bad starting point. The XenDesktop Design Handbook provides formulas for ballpark physical CPU cores and RAM based on user count/type and OS.

## Verwante notities

- [Citrix Project Accelerator: web-based design guidance](citrix-project-accelerator.md)
- [Delivery Controller server sizing and supported OS](delivery-controller-sizing.md)
- [Bas on IOPS, latency and storage sizing](iops-and-latency-fundamentals.md)
- [MCS rollbacks and reboot considerations (boot storms, disconnect policies)](mcs-rollbacks-and-reboot-considerations.md)
- [Bas's MCS storage implications checklist](mcs-storage-implications.md)
- [PowerFuse performance shields (reference)](powerfuse-performance-shields.md)
- [Bas on sizing: there is no 'one size fits all', and don't overdo it](sizing-no-one-size-fits-all.md)
- [Sizing resources: XenDesktop Design Handbook and community calculators](sizing-resources-and-handbook.md)
- [How memory works in Terminal Server: shared executables](terminal-server-memory-shared-executables.md)
- [Why the page file matters in Terminal Server](terminal-server-page-file-copy-on-write.md)
- [The five VDI workload phases and boot/logon storms](vdi-five-phases-storms.md)
