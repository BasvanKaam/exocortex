---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [launch-process, netscaler, hsd, sta, load-balancing]
layer: reference
bron: inside-citrix-fma
---

# External launch process: Hosted Shared Desktop via NetScaler

Launching a published Hosted Shared Desktop (XenApp) externally through NetScaler:

1. User clicks the icon; the launch request goes to NetScaler Gateway, then to StoreFront.
2. StoreFront contacts the Broker (XML/STA) service to find where the resource is available and best started, invoking the XenApp load-balancing mechanism (policy-configured as of XenApp 7.x).
3. StoreFront requests an STA ticket from the Broker service, including user, domain and resource name, plus a request for a 'least loaded' server.
4. The Broker (XML/STA) service queries the Central Site Database (ports 1433/1434) for the current Farm state, then applies its load-balance algorithm to pick a server.
5. The Broker creates the STA ticket (server + resource to connect to) and returns it to StoreFront as an XML-formatted file.
6. StoreFront generates a launch.ica file (from default.ica template) containing the STA ticket, connection properties, and the NetScaler Gateway FQDN, and passes it down through NetScaler to the local Receiver.
7. Receiver auto-launches the launch.ica file, connecting to NetScaler Gateway over 443/SSL.
8. NetScaler contacts the Broker (XML/STA) service to verify the STA ticket is still valid; the STA validates from memory and returns the target IP/port/resource name, then deletes the ticket.
9. NetScaler sets up a new ICA connection over port 1494 (ICA) or 2598 (CGP); the VDA verifies its license with a Delivery Controller; the Delivery Controller checks the Citrix License Server (and Microsoft CALs); Citrix policies are applied to the VDA.
10. The HSD session launches with NetScaler Gateway acting as proxy. Windows authentication occurs between the domain controller and the Citrix Worker/Session Host; the session initializes (profile load, GPOs, scripts, drive/printer mappings); session info is registered in the Central Site Database for future load balancing.

FMA fact: the STA ticket is generated and sent back after a user launches an application/desktop, not during resource enumeration, and it includes the resource and the server to launch it on (load balance).
