---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [netscaler, authentication, storefront, beacons, ldap]
layer: reference
bron: inside-citrix-fma
---

# External user authentication through NetScaler

When a user logs in externally through NetScaler Gateway (preferably SSL over port 443):

1. The user connects to the NetScaler Gateway external URL and enters credentials; a locally installed Receiver can also connect directly. Receiver uses Beacons to determine whether a connection is internal or external.
2. An EPA (End Point Analysis) scan may run as part of a SmartAccess/SmartControl policy; nFactor (multi-factor) authentication is optional as of NetScaler 11.0 build 62.x.
3. NetScaler authenticates credentials against Active Directory (preferably TCP 636 SSL) per the Authentication Policy; two-factor/RADIUS is considered a must-have minimum. NetScaler has its own Authentication Service.
4. NetScaler assigns a session cookie (it does not build the authentication token during initial authentication).
5. The session and credentials are redirected to StoreFront (per the Session Policy), which performs a call-back to the NetScaler Gateway virtual server to validate the user. Details go to the StoreFront Authentication Service.
6. The authentication token is built here (by default by the StoreFront Authentication Service, or via XML-based authentication as of StoreFront 3.0/3.5).
7. Credentials are forwarded as an XML query to the Broker (XML) service on a Delivery Controller (port 80 default, changeable to 443).
8. StoreFront checks its local datastore for existing subscriptions, storing them in memory.
9. The Broker (XML) service contacts a domain controller (port 389 default, 636 for SSL) to validate credentials and discover the user's security group SIDs.

You effectively validate against LDAP three times: via NetScaler (session cookie) to AD; via StoreFront/XML service to AD (builds the token); and via the XML service to AD (to find security group SIDs for enumeration). The Delivery Controller then queries the Central Site Database (ports 1433/1434) for assigned resources, returns them as an XML-formatted file, and StoreFront generates the resource web page routed back through NetScaler.

FMA fact: if you don't enable authentication on the NetScaler login page, NetScaler contacts StoreFront and the user is presented with the StoreFront login page (Receiver for web sites), with StoreFront handling authentication.

## Verwante notities

- [Bas's distinction between authentication and verification](authentication-vs-verification-distinction-2.md)
- [Bas's key takeaways on the user login process](bas-key-takeaways-user-login-process.md)
- [Beacon-based Receiver connection routing](beacon-based-receiver-connection-routing.md)
- [Citrix Site policies: Entitlement, Assignment, Site Access](citrix-site-policies-powershell.md)
- [A Citrix external logon validates against LDAP three times](citrix-three-ldap-validations-logon.md)
- [CWC StoreFront hosting options](cwc-storefront-options.md)
- [Desktop Appliance sites for non-domain-joined machines](desktop-appliance-sites.md)
- [External launch process: Hosted Shared Desktop via NetScaler](external-launch-process-hsd-netscaler.md)
- [NetScaler ADC vs NetScaler Gateway](netscaler-adc-vs-gateway.md)
- [NetScaler Gateway remote-access traffic flow](netscaler-gateway-traffic-flow.md)
- [NetScaler SNIP, STA tickets and certificate practice](netscaler-snip-and-sta.md)
- [NetScaler Unified Gateway](netscaler-unified-gateway.md)
- [Optimal NetScaler Gateway routing](optimal-netscaler-gateway-routing.md)
- [Configuring Receiver connection information](receiver-connection-configuration-methods.md)
- [The Secure Ticket Authority (STA)](secure-ticket-authority-sta.md)
- [Securing StoreFront connections with SSL and NetScaler](securing-storefront-connections-with-ssl.md)
- [StoreFront authentication and resource enumeration traffic flow](storefront-authentication-traffic-flow.md)
- [StoreFront vs Web Interface user authentication](storefront-vs-web-interface-authentication.md)
