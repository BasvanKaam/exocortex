---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [nerdio, wvd, avd, autoscale, personal-desktop, rbac, cost-optimization]
layer: reference
gedateerd: ja
bron: nerdio-blog
---

# Nerdio autoscaling for personal/persistent desktops

Autoscale knobs differ for single-user personal (persistent) desktops versus pooled. Each user gets a dedicated, permanently assigned host VM usable only by them.

## Assignment type
- **Automatic**: users are assigned to an available desktop VM on first login (can also be manually pre-assigned).
- **Direct**: users must be pre-assigned to a VM before they can log in.

## Power controls
- **Working hours**: the days/hours these VMs should be on.
- **Power off aggressiveness** (applied at end of working hours):
  - **High**: powers off all VMs including those with active/disconnected sessions; active-session users get a message and time to log off first.
  - **Medium**: powers off only VMs with no active session (disconnected is OK to power off).
  - **Low**: powers off only VMs with no active and no disconnected sessions.
- **Power on timing**: *Once* (powered on once at start of working hours; not re-powered if a user shuts it off later) or *Continuously* (auto-scale re-powers any manually powered-off VM during working hours).
- **Power off timing**: *Once* (powered off at end of day per aggressiveness; manual power-ons outside hours are left alone) or *Continuously* (also auto-powers-off VMs manually started outside hours, subject to aggressiveness).
- **Messaging**: warn users 10/15/30/45/60 min before power-off. Only applies when aggressiveness is High (Medium/Low never stop active-session hosts).

## End-User RBAC role
A built-in Nerdio role letting end users log into the console to start, stop, and restart their own assigned desktop, and log off their own active sessions (personal or hosted-shared). Mix-and-match power-off timing + aggressiveness + this role to cover almost any use case. Example: timing Continuously + aggressiveness Medium/Low means the VM shuts down when the session is disconnected/inactive at end of day; if the user later powers it back on via the end-user role, it stays up while the session is active, and eventually shuts down on idle/disconnect policy.

*Bron: Nerdio-content 'How to get the most out of your personal assigned VMs on WVD at the lowest cost possible' (Blogs).*

## Verwante notities

- [Don't leave desktop power management to users alone](dont-leave-power-management-to-users.md)
- [Nerdio autoscaling engine: pooled hostpool scaling logic](nerdio-autoscaling-engine-pooled-hostpools.md)
- [Nerdio self-service portal: delegated machine control for power users](nerdio-self-service-portal-user-control.md)
- [Static vs dynamic host pools in Nerdio (autoscale eligibility)](nerdio-static-vs-dynamic-host-pools.md)
- [Microsoft's WVD power scripts are not real autoscaling](nerdio-vs-microsoft-power-management-scripts.md)
- [What the Nerdio autoscale engine does (NMW era)](nmw-autoscale-engine-capabilities.md)
- [Single-User vs Multi-User VDI/DaaS](single-user-vs-multi-user-vdi-daas.md)
