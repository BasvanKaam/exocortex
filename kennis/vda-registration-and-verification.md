---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [vda, registration, troubleshooting, delivery-controller]
layer: rich
bron: inside-citrix-fma
---

# VDA registration and how to verify it

Key VDA facts Bas wants remembered:

- On boot, a VDA registers itself with a Delivery Controller; the mechanism to find one is called 'auto-update' (other methods exist too).
- Registration uses port 80 by default; this can be changed via VDA settings in Control Panel.
- If a VDA cannot register, it stays in an unregistered state and is not directly accessible or manageable through a Delivery Controller.
- A VDA has two main services: the Citrix Desktop Service and the Citrix ICA Service. The Desktop Service talks to the Broker service on the Controller it registers with.
- Restarting the Citrix Desktop Service on the VDA forces re-registration; afterwards look for event 1012 confirming successful registration.
- Power management (the Controller (re)booting the machine and telling it to listen for new connections) works for desktop VDAs only.
