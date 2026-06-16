---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [broker, xml, sta, vda-registration, load-balancing]
layer: reference
bron: inside-citrix-fma
---

# FMA Broker Service (XML/STA) and its responsibilities

The Broker (XML) Service is the best-known FMA service. From a Delivery Controller view it brokers new and manages existing sessions, handles resource enumeration, STA ticket creation/verification, user validation, disconnected sessions and more. From a VDA view it handles all communication to/from the Controller by talking to the VDA's Citrix Desktop Service (BrokerAgent.exe).

The STA Service has been part of the Broker Service since Presentation Server 4.0 (before that it was an ISAPI extension for IIS). As of XenDesktop 4.x the XML service (ctxxmlss.exe) was rewritten in .NET and became part of the Broker Service.

The Broker Service is built from three separate services (four if you count the Principal Broker Service): it brokers connections, enumerates resources, can handle authentication tokens, acts as the Secure Ticket Authority (only for resources launched through a NetScaler), and as of 7.12 is involved in managing the Local Host Cache.

Main responsibilities include: VDA registration, resource allocation, connection brokering, licensing enforcement, XML-based authentication, HDX policy management, power state management (start/stop VMs, idle pool management, reboot schedules, remote PC wake-on-LAN), temporary SSO credential storage, tracking virtual desktop state, and initial load balancing (decision ends up in the ICA launch file).

## Verwante notities

- [Broker Service: XML, STA and the Principal Broker](broker-service-xml-sta-principal.md)
- [The Broker Service bundles brokering, XML and STA in one process](citrix-broker-service-three-roles.md)
- [Citrix Site policies: Entitlement, Assignment, Site Access](citrix-site-policies-powershell.md)
- [The Delivery Controller as the heart of the FMA](delivery-controller-heart-of-fma.md)
- [External launch process: Hosted Shared Desktop via NetScaler](external-launch-process-hsd-netscaler.md)
- [The eighteen Broker Service Site services (distributed housekeeping)](fma-broker-eighteen-site-services.md)
- [The four most prominent FMA core services](fma-four-prominent-core-services.md)
- [The Secure Ticket Authority (STA)](secure-ticket-authority-sta.md)
- [VDA registration and how to verify it](vda-registration-and-verification.md)
