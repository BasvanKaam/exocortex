---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [fma, wcf, port-80, endpoint, db-connection-string]
layer: reference
bron: inside-citrix-fma
---

# FMA internal communication over WCF endpoints (port 80)

Although FMA services run completely isolated from each other, internal communication takes place using WCF (Windows Communication Foundation) endpoints (also called service interfaces) over port 80 by default. Port 80 can be changed to any port, and encryption is supported.

The endpoint address is represented by the EndpointAddress class, containing a URI representing the service address (a secure identity plus optional Headers). Each service can interact with all others.

FMA fact: each service is configured to communicate to the Central Site database using its own individual DB connection string, so if one service fails it does not affect the others. Note: if you change something for one service (like the DB connection string) you must do it for all the other FMA services as well.

All FMA services run under the NT AUTHORITY\Network service account; when authenticating to the Central Site database they use the local computer account of the machine they run on.

## Verwante notities

- [FMA services: Network Service account and service isolation](fma-services-network-account-and-isolation.md)
