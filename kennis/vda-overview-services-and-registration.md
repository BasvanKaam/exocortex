---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [vda, registration, auto-update, listofddcs, services]
layer: reference
bron: inside-citrix-fma
---

# The VDA: client-side component, services and registration

The Virtual Delivery Agent (VDA) is a small piece of software installed on all virtual/physical machines running a Windows/Linux server or desktop OS in the Site, making their resources remotely available. It is the client-side component of the FMA: it registers with the Delivery Controller and communicates with the Receiver on the endpoint. During session brokering it establishes/manages the connection; at session initialization it checks for a valid Citrix license and applies configured policies.

FMA fact: before XenDesktop 7 the VDA was the Virtual *Desktop* Agent; today it is the Virtual *Delivery* Agent.

Two main services:
- Citrix ICA Service (picaSvc2.exe)
- Citrix Desktop Service (BrokerAgent.exe), which talks directly to the Broker Service on the Controller. The Desktop Service hosts plug-ins (Director plug-in, WMI plug-in, Monitor plug-in and more), all communicating with the Controller through it.

Registration: on OS boot the VDA tries to register with a known Controller. The 'auto-update' feature (enabled by default) keeps VDAs informed as Controllers are added/removed; each VDA stores this info persistently. If auto-update is disabled or wrong, the VDA checks, in order: configured policies, the ListOfDDCs registry key, OU-based discovery (legacy), the Personality.ini file created by MCS. Registration uses port 80 by default. FMA fact: a VDA that cannot register stays 'unregistered' and is not directly accessible/manageable. Verify registration by restarting the Citrix Desktop Service and looking for event 1012.

## Verwante notities

- [Desktop VDA core services: Citrix Desktop Service and Citrix ICA Service](desktop-vda-two-main-services.md)
- [Linux VDA install dependencies and ctxsetup.sh configuration](linux-vda-install-config-dependencies.md)
- [PortICA / picaSvc2.exe: the critical VDA ICA service](portica-picasvc2-service.md)
- [Server VDA vs Desktop VDA: the often-overlooked new component](server-vda-vs-desktop-vda.md)
- [Two VDA types and the single-user vs multi-user ICA stack](two-vda-types-ica-stack-difference.md)
- [VDA install options and supported operating systems](vda-install-options-and-supported-os.md)
- [VDA registration and how to verify it](vda-registration-and-verification.md)
- [VDA registration: auto-update, fallback locations and the CBP](vda-registration-process.md)
- [Troubleshooting the VDA registration process and Citrix Health Assistant](vda-registration-troubleshooting.md)
