---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [printing, ctx-print-management, ica, virtual-channel]
layer: reference
bron: inside-citrix-fma
---

# Citrix Print Management Service

The Citrix Print Management Service was first introduced in 2005, around the same time as the EMF-based universal print driver. It directly communicates with the Print Spooler service and, when the client printing pathway is used, communicates with the locally installed ICA Client and compresses data before it's sent over the ICA channel. It is in charge of the ICA virtual channel for client printer mapping/creation within the CTX session, which is useful to know when troubleshooting auto-create printer failures.
