---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [storefront, ssl, netscaler, security, vda]
layer: reference
bron: inside-citrix-fma
---

# Securing StoreFront connections with SSL and NetScaler

Internal communication from a web browser or Citrix Receiver to StoreFront initially contains user credentials, passwords included. When users log in remotely (from home), that same information traverses the unsecured Internet, so all traffic should be secured and encrypted using SSL (Secure Sockets Layer). A NetScaler is the recommended approach for secure remote access.

To set up SSL, trusted certificates must be installed on all StoreFront servers and on the NetScalers. Companies with high security standards can extend the same to traffic between StoreFront servers and Delivery Controllers, and even further to all installed VDAs (requiring extra planning and maintenance).

As of version 7.6, SSL was integrated into the core of the Citrix VDA, making it much more straightforward to enable on all machines and connections. It works for XenDesktop as well as XenApp, and for persistent as well as non-persistent desktops. There may be a slight but negligible performance impact.

## Verwante notities

- [CWC authentication and credential handling security](cwc-authentication-credential-handling.md)
- [CWC StoreFront hosting options](cwc-storefront-options.md)
- [External user authentication through NetScaler](external-authentication-through-netscaler.md)
- [NetScaler SSL certificates and certificate trust](netscaler-ssl-certificates-and-trust.md)
- [NetScaler SSL offloading and DMZ placement](netscaler-ssl-offload-dmz.md)
- [StoreFront authentication and resource enumeration traffic flow](storefront-authentication-traffic-flow.md)
- [Wildcard and SAN certificates](wildcard-and-san-certificates.md)
