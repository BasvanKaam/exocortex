---
type: kennis
merk: nerdio
domein: nerdio
status: actief
datum: 2026-10-02
tags: [nerdio, nme, console-connect, agent, deployment, troubleshooting, intune, notes-from-the-field]
layer: reference
gedateerd: ja
bron: nerdio-university-lesson
---

# Console Connect agent deployment and the connection path

Lesson 3 of the Console Connect track in Bas's "Notes from the field" series, for administrators (prerequisites: the first two lessons, an admin role or read access to the region configuration, and familiarity with Windows services and event logs). Promise of the lesson: a device that reports Not installed is no longer a mystery, "it's a question with four possible answers and a way to tell them apart."

## The four moving parts
- **Nerdio Manager:** holds the region configuration, decides scope, generates the deployment tasks, and creates the session when a technician selects Connect.
- **Regional service:** the broker. Tracks which devices are online and accepting connections, and issues the session token.
- **Agent:** a Windows service on the device, present with or without a signed-in user (unattended access).
- **Browser:** holds the session; nothing is installed on the technician's device.
Zoho provides the underlying infrastructure, so service domains and the agent carry Zoho names.

## Three deployment routes
- **Session hosts:** enrolling a host pool in a region generates tasks that install the agent on existing hosts and every later host, including auto-scale, via the Azure Custom Script Extension.
- **Intune-managed endpoints:** NME creates a device group and deploys the agent with a platform script targeted at it. Requires the Intune Applications and App policies permission set to Manage, not Read-only.
- **Desktop images:** installed on demand when you connect; a dialog asks for the region and the session starts once installation finishes.
- Per-device trigger: connecting to a session host that missed its install starts the deployment instead of failing.
- No separate installer download; only devices NME manages can be reached.

## Footprint on the device
- A regular Windows installer package. A service in session 0 (reachable with nobody signed in), a component in the user session (what the technician sees interactively), and a third that starts on connect.
- Listed in Programs and Features under its Zoho name; files in the ZohoMeeting folder under Program Files. Tell the security team in advance: an unexplained remote-access agent starts incidents.
- Antivirus and endpoint protection need the agent directories excluded and the service and executables allowed. This is the most common reason an install completes but the device never reports Online.

## Verify a deployment
From NME: Filter by CC status on Session Hosts, Servers and Intune Devices; look for Not installed. Make it part of finishing every rollout. On the device, in this order:
1. Agent service present and running.
2. Agent listed in Programs and Features.
3. NME installation log in the log folder under `C:\Windows\Temp`.
4. Windows event log: installer events under Application, service install and start under System.
5. Installed but not Online: agent logs at `%programdata%\ZohoMeeting\log`.
Steps 1 and 2 split deployment problems from connectivity problems. "Guessing between those two turns a 10-minute step into an afternoon."

## The connection path
1. Browser asks NME for a session.
2. NME requests a session token from the regional service.
3. Service verifies the device exists, is online and accepts connections.
4. Token goes back to NME, which passes it to the browser.
5. Browser opens a new tab and the session starts.
NME records a task per attempt, named by context (AVD session host, Intune device, desktop image): the first place to look, because it shows whether the request reached NME at all. A powered-off device or a device network problem stops at step 3: a connection that never starts, not a session that breaks. The status column tells them apart.

## Four causes of a failed deployment (none on the device itself)
- Outbound access blocked (firewall, proxy, SSL inspection) to the region-specific service domains; an exclusion for one region does not cover another.
- Antivirus quarantines the agent: install completes, device Offline.
- Intune permission Read-only: the Intune device group option never shows, so endpoints were never in scope.
- Devices outside the Intune scope: NME's validation warning gives the skipped count.
Check the region configuration before touching a device: a device never added to a region is not broken, it is not enrolled.

## Knowledge checks (answers)
- Layers: Intune group option missing = Permissions; installed but Offline = Device; Connect missing for a new host pool = Region configuration; fails behind one proxy = Network.
- Mechanisms: session host = Azure Custom Script Extension; Intune endpoint = platform script; desktop image = installed on demand when you connect.

## Verwante notities

- [Notes from the field: Bas's Nerdio lesson series](nerdio-notes-from-the-field.md)
- [Plan and scope Console Connect for help desk teams](console-connect-plan-and-scope-help-desk.md)
- [Use Console Connect for end-user and session host support](console-connect-end-user-and-session-host-support.md)
