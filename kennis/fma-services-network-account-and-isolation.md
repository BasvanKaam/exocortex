---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [fma, services, security, architecture, wcf]
layer: rich
bron: inside-citrix-fma
---

# FMA services: Network Service account and service isolation

The FMA grew from six up to eleven main services over the years. Internal communication runs over port 80 using Windows Communication Foundation (WCF) endpoints.

Each service runs completely separated from the others with its own database connection string, so a single service failure does not directly affect the others — but the flip side, Bas warns, is that if you change something like the DB connection string you must change it for every FMA service.

All services run under the NT AUTHORITY\Network Service account and authenticate to the database using the local computer account of the machine they run on. Bas highlights a real benefit: passwords are automatically rotated every 30 days, which matters because service accounts are usually very dangerous. Refreshing a service's cache (it holds the services listing, retrieved at startup, refreshed roughly every five minutes) is as simple as restarting the accompanying Windows Service. The Configuration Service stores configuration metadata for all services, relieving Active Directory.

## Bron-citaten (NL, verbatim)

> This is a big deal, as service accounts are usually very dangerous.

## Verwante notities

- [FMA Configuration Service: the glue holding the FMA together](fma-configuration-service.md)
- [FMA foundation: .NET, WCF, CLR and just-in-time compilation](fma-foundation-dotnet-wcf-clr.md)
- [The four most prominent FMA core services](fma-four-prominent-core-services.md)
- [FMA internal communication over WCF endpoints (port 80)](fma-internal-communication-wcf.md)
- [FMA service high availability via peer service groups](fma-services-high-availability.md)
- [FMA services run independently, with separate DB connection strings](fma-services-independent-registry-accounts.md)
- [The FlexCast Management Architecture and its thirteen core services](fma-thirteen-core-services-overview.md)
