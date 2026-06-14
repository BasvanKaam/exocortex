---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [storefront, authentication, xml, enumeration, kerberos]
layer: reference
bron: inside-citrix-fma
---

# StoreFront authentication and resource enumeration traffic flow

Within a Site there are two authentication points: StoreFront and the NetScaler Gateway. StoreFront communicates with Receiver, the Delivery Controllers and (for external auth) the NetScaler STA. It is the main Store from which users subscribe to desktops and apps.

Users authenticate to StoreFront via username/password, Domain pass-through, NetScaler pass-through, smart cards, or unauthenticated access. The internal authentication service is integral to StoreFront. Internal login flow:
1. User submits credentials; StoreFront's authentication service authenticates them with a domain controller.
2. StoreFront forwards the credentials as an XML query to a configured Delivery Controller (meanwhile checking its local datastore for existing subscriptions, held in memory). Kerberos delegation is optional.
3. The Controller contacts a domain controller again to validate the credentials, then responds to StoreFront.
4. The Controller checks the Central Site database for resources assigned to the user.
5. It sends those resources back to StoreFront.
6. StoreFront generates a web page showing the resource icons.

Web Interface (EOL June 2018) works differently: it has NO internal authentication service and immediately forwards credentials as an XML query to a Controller. Citrix recommends StoreFront for new and existing deployments. As of StoreFront 3.0, XML-based authentication was reintroduced (a few PowerShell scripts make auth fall back to the XML service like Web Interface), useful when StoreFront is in a different domain or no AD trust is possible; disabled by default.

## Verwante notities

- [Bas's distinction: authentication versus verification](authentication-vs-verification-distinction.md)
- [Beacon-based Receiver connection routing](beacon-based-receiver-connection-routing.md)
- [Broker Service: XML, STA and the Principal Broker](broker-service-xml-sta-principal.md)
- [A Citrix external logon validates against LDAP three times](citrix-three-ldap-validations-logon.md)
- [Desktop Appliance sites for non-domain-joined machines](desktop-appliance-sites.md)
- [External user authentication through NetScaler](external-authentication-through-netscaler.md)
- [Internal launch process: pooled VDI VM via StoreFront](internal-launch-process-pooled-vdi.md)
- [Securing StoreFront connections with SSL and NetScaler](securing-storefront-connections-with-ssl.md)
- [StoreFront over Web Interface, and StoreFront design notes](storefront-over-web-interface.md)
- [StoreFront vs Web Interface user authentication](storefront-vs-web-interface-authentication.md)
- [StoreFront authenticates locally, Web Interface delegates via XML](storefront-vs-webinterface-auth-flow.md)
- [Launching a VDI desktop from a trusted internal network](vdi-desktop-launch-sequence.md)
- [XenApp Services URLs for legacy Receiver access](xenapp-services-urls-legacy-access.md)
