---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [receiver, storefront, beacons, netscaler, connection-routing]
layer: reference
bron: inside-citrix-fma
---

# Beacon-based Receiver connection routing

Citrix Receiver, combined with StoreFront, uses Beacons to determine whether a connection is made internally or externally, then routes it accordingly. Beacons are simply basic URLs used by Receiver to determine its location.

When a connection is made, Receiver tries to contact the beacon points (URLs) to determine where the connection originated. It starts with any internal-configured beacons, then moves to external if no match is found. Based on the outcome, the location information is forwarded to the server providing the resources, and the connection is routed either externally through the NetScaler Gateway or internally through StoreFront.

This simplifies user access: you don't need two separate URLs (one internal, one external). Combined with email-based discovery, users just download Receiver, fill in their email address, and they are good to go.

FMA fact: By default, StoreFront uses your internal services URL as the internal resolvable Beacon point and Citrix.com as the external Beacon point. These can be changed to anything you like, but ensure the internal Beacon is not resolvable externally.

## Verwante notities

- [Citrix CloudGateway: AppController, StoreFront and Access Gateway](citrix-cloudgateway-architecture.md)
- [Citrix Receiver: purpose and naming history](citrix-receiver-history-and-purpose.md)
- [External user authentication through NetScaler](external-authentication-through-netscaler.md)
- [Optimal NetScaler Gateway routing](optimal-netscaler-gateway-routing.md)
- [Configuring Receiver connection information](receiver-connection-configuration-methods.md)
- [Three ways to reach resources via Receiver, including HTML5 clientless access](receiver-three-ways-and-html5-clientless.md)
- [StoreFront authentication and resource enumeration traffic flow](storefront-authentication-traffic-flow.md)
