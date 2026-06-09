---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [bas-takeaways, authentication, verification, sta, troubleshooting]
layer: rich
bron: inside-citrix-fma
---

# Bas's key takeaways on the user login process

Bas's takeaways for the login/launch chapter:

- There are two main authentication points in the FMA: NetScaler (optional) and StoreFront.
- Knowing the difference between IMA and FMA, how traffic flows, and how components interact is vital to troubleshooting the FMA.
- As of version 3.0, StoreFront can also use the XML service to authenticate users.
- He stresses a distinct difference between authentication and verification: authentication makes sure somebody is who they claim to be; verification finds out which resources (permissions) are assigned to the user, which then show in the store ready for subscription.
- User authentication and resource enumeration go hand-in-hand.
- The STA only applies for external connections through NetScaler, and the STA service is part of the Broker server (as is the better-known XML service).
- The HTML5-based Receiver offers the same functionality as a natively installed Receiver.
- The Windows authentication process is also involved when launching a Citrix published resource.
- Site policies let you exclude users or apply policies under specific conditions, managed via PowerShell.

He sums up his troubleshooting philosophy: 'if you don't know or understand the basics of what you are dealing with, then you're bound to get lost, fast.'

## Bron-citaten (NL, verbatim)

> if you don't know or understand the basics of what you are dealing with, then you're bound to get lost, fast.
