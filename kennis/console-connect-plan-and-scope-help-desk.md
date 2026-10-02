---
type: kennis
merk: nerdio
domein: nerdio
status: actief
datum: 2026-10-02
tags: [nerdio, nme, console-connect, help-desk, rbac, session-shadowing, notes-from-the-field]
layer: reference
gedateerd: ja
bron: nerdio-university-lesson
---

# Plan and scope Console Connect for help desk teams

Lesson 1 of the Console Connect track in Bas's "Notes from the field" series. The question it answers: when a help desk retires a separate remote-support tool in favor of Console Connect, how do you give support staff exactly the access they need without full administrative rights to Nerdio Manager for Enterprise (NME)?

## Console Connect versus session shadowing
- **Session shadowing** is the older native capability: direct RDP to view or control an active session. Needs network line-of-sight to the session host and works on multi-session Windows only. Advantages: no agent, stays inside your own network.
- **Console Connect** routes through a cloud-hosted regional broker over TLS on TCP 443 (registration, session and file transfer), so no line-of-sight or VPN. Reaches single-session AVD, Windows 365 Cloud PCs, desktop images, Intune-managed physical endpoints, Windows Servers, and devices with nobody signed in.
- Extra capabilities: unattended access (Toolbox session), Toolbox tools (PowerShell, Windows services, Task Manager, Registry Editor), diagnostics, file transfer, reconnect through a reboot while the browser tab stays open, and an optional end-user confirmation set per region.
- Practical rule: a team that only supports multi-session AVD from inside the network can keep shadowing; as soon as it supports anything else, Console Connect covers it all from one place.

## Regions, capacity, licensing
- Regions: United States, United Kingdom, EU, Canada, Japan, Australia. Each region brokers its own traffic; pick by data residency.
- Capacity: 5,000 devices per region by default; Nerdio support can raise it.
- Licensing: included in the existing AVD, Windows 365 and physical endpoint SKUs.
- Region configuration (System > Settings > Integrations > Console Connect) decides reach: add host pools, Windows 365 provisioning policies and Intune device groups. Select All does a one-time import of all host pools.
- Session confirmation: custom prompt on the user's desktop, Yes or No. Typical for office-hours help desks; usually off for overnight maintenance, because nobody answers the prompt.
- NME v8.0 added Allow uninstall (local users can remove the agent). Decide first: the device stays unreachable until an admin redeploys.
- Branding: display name and favicon per region; empty means Nerdio branding.
- REST API: enable or disable for host pools and regions, and get the session URL for Intune devices.
- Before handover: Filter by CC status on Session Hosts, Servers and Intune Devices, look for Not installed. After go-live: View Statistics shows usage (adoption, not what happened in a session).

## Scope help desk access with a custom role
- Full administrator includes Console Connect by default; too much for most help desk staff.
- Create a custom role: System > RBAC > Definitions > New Definition, module permission **Manage Sessions**. Assign at System > RBAC > Assignments (role, users or groups, AVD tenant).
- The built-in Help Desk role deliberately has no Console Connect access, so remote access to devices stays an explicit decision.
- **Console Connect Operator** is a separate mode in two modules: Workspaces (AVD & Sessions) and Intune. No single permission covers both. A tier that also handles Cloud PCs and Intune endpoints needs the Intune module too. The Operator can connect but not decide who else can.
- Tiering: first line needs Manage Sessions only; a tier that also manages host pool configuration may add a broader Workspaces permission, but every added permission broadens the role outside Console Connect.
- Toolbox access via a custom role is currently all-or-nothing (including PowerShell and Registry Editor); more granular permissions are planned. Mind this for outsourced or junior staff.

## Current limitations
- No action logging and no session recording. The session details page shows who connected and when, not what they did. Plan for the audit gap up front.
- One technician per device at a time; a second connection takes over and the first loses visibility. For a second observer, pair with a separate screen-sharing tool.

## Knowledge checks (answers)
- Console Connect but not shadowing: single-session AVD, Windows 365 Cloud PCs, file transfer.
- Technician abruptly disconnected with no error: first check whether another technician connected to the same device.
- Full admin = access plus full rights; custom role with Manage Sessions = session management plus Console Connect; built-in Help Desk = no access by design.

## Verwante notities

- [Notes from the field: Bas's Nerdio lesson series](nerdio-notes-from-the-field.md)
- [Use Console Connect for end-user and session host support](console-connect-end-user-and-session-host-support.md)
- [Console Connect agent deployment and the connection path](console-connect-agent-deployment-connection-path.md)
- [Mapping Zero Trust Principles to Real NME Capabilities](mapping-zero-trust-to-nme-capabilities.md)
