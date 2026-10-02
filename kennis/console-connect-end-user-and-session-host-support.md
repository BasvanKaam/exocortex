---
type: kennis
merk: nerdio
domein: nerdio
status: actief
datum: 2026-10-02
tags: [nerdio, nme, console-connect, help-desk, troubleshooting, toolbox, notes-from-the-field]
layer: reference
gedateerd: ja
bron: nerdio-university-lesson
---

# Use Console Connect for end-user and session host support

Lesson 2 of the Console Connect track in Bas's "Notes from the field" series. Opening problem: in a pooled host pool with breadth-first load balancing, any of several session hosts can get a user's connection, and a traditional remote desktop connection needs line-of-sight to that exact host. The lesson covers choosing a session type, connecting to every endpoint type, the in-session tools, and troubleshooting.

## Interactive or Toolbox
- **Interactive user session:** you see and control what the user sees, with an optional confirmation prompt.
- **Toolbox session:** leaves the user's desktop alone. PowerShell, Windows services, Task Manager, Registry Editor; works with no user signed in. Reconnects if the browser tab stays open through a reboot or sign-in. UAC prompts on the target still apply.
- The Console Session dialog also lists the **console session** (the machine's primary display session). On a single-session host, signing in to it as another account signs the current user out; on multi-session it interrupts nobody.
- Rule of thumb: interactive when you need to see what the user sees (an app error together); Toolbox to diagnose without disturbing a user (a host that stopped accepting connections, a hung service).
- Both types: file transfer, clipboard sync, in-session chat with optional audio and video, visual annotations.

## Connecting
- Only Windows endpoints; the technician's own device and browser can run any OS. Only devices managed by NME.
- **AVD session host:** more options > Connect > Interactive user session > OK; console opens in a browser tab; Diagnostics for command prompt or PowerShell; exit icon > End now; review the summary > Close Page. Hosts in an enrolled pool get the agent automatically, including new auto-scale hosts.
- **Windows 365 Cloud PC:** Connect from the Cloud PC action menu. **Intune endpoint:** Endpoints > Intune > All Devices > Connect. Same flow from the dialog onward; no VPN for remote workers.
- **Toolbox:** pick Toolbox in the dialog; tools in the left menu, output on the right; PowerShell area and Run as.
- **Desktop image:** Cloud Desktops > Desktop Images > more actions > Connect; select region and install the agent if prompted. The agent installs on the running image VM and is excluded from the sysprepped output. Do not bake it into a captured image. Removes the need for a jump box or VPN when managing images.

## Tools in an active session
Left menu groups: View (size, full screen, color, resolution), Session, Tools (run a script file, power options: Lock Screen, Log Off, Reboot, Reboot in Safe Mode, Shutdown), Files (send and receive with progress), Chat, Diagnostics (command prompt, PowerShell, Task Manager, Device Manager, Task Scheduler, services, printers, hardware, groups, software, users).
Session menu: Send Alt+Tab, Send Ctrl+Alt+Del, Short Keys, Screenshot, Network Statistics, Disable Input Devices, Remote Audio, Blacken Screen (user can revoke with Ctrl+Alt+Del), Clipboard Sync.
- PowerShell script files run inside the session; NME scripted actions run from NME, not from the session.
- Sessions are not recorded and in-session tasks are not written to NME logs: record changes in the ticket.

## Troubleshooting
Flow: Connect > NME asks the region for device details > region validates the endpoint exists and is reachable > session opens. Most failures stop at validation, so check agent status first (Filter by CC status):
- **Not installed:** agent not deployed yet. **Offline:** installed, device not reachable; check it is powered on. **Online:** reachable; if it still fails, check your role has Console Connect access. **Other:** unexpected state; administrator investigates.

Recurring causes:
- Connect option missing: device not in the region configuration.
- Session fails on one device: outbound access. Exclude the listed domains and executables from firewall, proxy, SSL inspection and antivirus; open TCP 80 and 443 to the addresses from `nslookup gateway.console-connect.com`.
- Intune endpoint still Not installed: follows the Intune check-in cycle; run the Install Console Connect Agent task and restart to force a check-in.
- Manual install on one device: not possible, NME deploys the agent.
- No confirmation prompt: not enabled for that region (expected).
- Disconnected without warning: another technician connected.
- No reconnect after reboot: the browser tab was closed.
- Some devices in an Intune group skipped: outside the Intune scope; NME shows a validation warning with the count.
- Intune device group option missing: Intune Applications and App policies set to Read-only; set to Manage.
- No prompt although enabled: you rejoined a session a previous technician left open by closing the tab.
- The agent shows as Zoho Assist Unattended Agent and the exclusions include Zoho domains (Zoho provides the infrastructure). Tell the security team in advance.

## Knowledge checks (answers)
- Order: Connect > Interactive user session > Diagnostics > End now.
- Not installed: escalate to an admin to add the device or install the agent. Offline: confirm power first. Other: escalate.
- Toolbox fits: checking services on an unresponsive host without disturbing a connected user; running a PowerShell script outside business hours with nobody signed in.

## Verwante notities

- [Notes from the field: Bas's Nerdio lesson series](nerdio-notes-from-the-field.md)
- [Plan and scope Console Connect for help desk teams](console-connect-plan-and-scope-help-desk.md)
- [Console Connect agent deployment and the connection path](console-connect-agent-deployment-connection-path.md)
