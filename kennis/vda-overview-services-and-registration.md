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
