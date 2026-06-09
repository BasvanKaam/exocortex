---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [vda, registration, auto-update, cbp, troubleshooting]
layer: rich
bron: inside-citrix-fma
---

# VDA registration: auto-update, fallback locations and the CBP

When a VDA's OS boots it tries to register with one of the Delivery Controllers known in the Site. There must be a mechanism telling VDAs which Controllers exist and how to reach them. Citrix's **auto-update** feature (enabled by default) keeps all VDAs informed as Controllers are added or removed; each VDA keeps a persistent storage location for this.

When auto-update is disabled or wrong, the VDA checks (in order): configured policies, the ListOfDDCs registry key, OU-based discovery (legacy), and the Personality.ini file created by MCS.

If a VDA cannot register or communication fails, you cannot connect to it. Bas calls out from experience that **VDA registration is the number-one issue reported to Citrix support** and deserves extra attention.

The Citrix Desktop service (part of the installed VDA) communicates directly with the Broker service on the Controller and handles the initial registration via the **Connection Brokering Protocol (CBP)**, a collection of WCF endpoints. Restarting the Citrix Desktop service on the VDA triggers (forces) re-registration.
