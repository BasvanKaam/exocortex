---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [configuration-service, service-registration, wcf, caching, permissions]
layer: reference
bron: inside-citrix-fma
---

# FMA Configuration Service: the glue holding the FMA together

All FMA services must register with the Configuration Service on start-up. Located at the centre of the FMA, it holds and manages a list of all services, letting them advertise their WCF addresses/endpoints and the functionality they provide. Only after successful registration does a service become active and able to communicate.

When one service needs to talk to another it first contacts the Configuration Service for a copy of the services listing. This listing is then cached for five minutes to avoid overwhelming the Configuration Service and prevent it becoming a bottleneck. (Exception: the Machine Creation Service and Machine Identity Service query the Host Service for Host Connection info, cached for one minute instead of five.)

The Configuration Service directory stores the AD machine account identifier (SID) for each registered service (also stored in the Central Site database). Only services whose machine SID is listed can communicate; an unregistered machine account gets access denied, except the 'Network service' account which is always allowed.

Validate registration via PowerShell: `Get-ConfigRegisteredServiceInstance -InterfaceType sdk | select serviceaccount, interfacetype, servicetype | format-table`. To refresh a service's cache, simply restart the accompanying Windows Service (the listing is retrieved at start-up). The Configuration Service also stores configuration metadata for all services, relieving Active Directory.
