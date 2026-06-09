---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [vdi, launch, storefront, launch-ica, xml-service]
layer: reference
bron: inside-citrix-fma
---

# Launching a VDI desktop from a trusted internal network

When a VDI VM is launched (pre-subscribed, already on the user's StoreFront home screen):

1. The user clicks the desktop icon; StoreFront contacts the Broker (XML/STA) service to check for available registered VDAs, querying the hypervisor via the Host service.
2. If needed it first boots a VM (pre-booting a few VMs improves the user experience).
3. The VDA registers with the Controller via the CBP / Broker service.
4. The Controller (Broker XML/STA) sends a StartListening request to a VDA. By default the VDA isn't listening on port 494 or 2595 until notified a user wants to connect.
5. Once the VDA listens, the Broker sends this info back to StoreFront as an XML file.
6. StoreFront generates a launch.ica file (using default.ica as a template) with the VDA's IP and other connection properties, sent to the user.
7. The local Receiver (or HTML5 Receiver) reads and auto-launches launch.ica, initiating a direct connection from endpoint to VDA.
8. The VDA verifies its license with the Controller; the Controller checks the Citrix License Server for a valid ticket (a change from IMA, where every Session Host talked to the license server).
9. Applicable session policies are passed to the VDA and the session launches.
