---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [launch-process, vdi, storefront, vda, ica]
layer: reference
bron: inside-citrix-fma
---

# Internal launch process: pooled VDI VM via StoreFront

Launching a pooled VDI virtual machine internally (no NetScaler, so no STA involved):

1. User clicks the (pre-subscribed) icon; StoreFront contacts the Broker (XML) service on the Delivery Controller to check for available registered VDAs, communicating with the hypervisor (Host Connection) via the Host service on the Delivery Controller.
2. If needed, a VM is started/booted first (pre-booting a few VMs is common and improves user experience).
3. The Delivery Controller/Broker service sends a startlistening request to a VDA. By default the VDA isn't listening for new connections on port 1494 or 2595 until notified.
4. Once listening, the Broker service returns this info to StoreFront as an XML-formatted file (not an actual XML file).
5. StoreFront generates a launch.ica file (from default.ica template) containing the VDA IP and connection properties, sent to the Receiver.
6. The local (or HTML5) Receiver auto-launches launch.ica, making a direct endpoint-to-VDA connection via ICA over port 1494.
7. The VDA verifies its license with the Delivery Controller; the Delivery Controller checks the Citrix License Server for a valid ticket; Citrix policies are applied to the VDA.
8. Windows authentication occurs between the domain controller and the Citrix VDI VM; the session initializes (profile load, GPOs, scripts, drive/printer mappings); session info is registered in the Central Site Database; the VDI session is fully launched.
