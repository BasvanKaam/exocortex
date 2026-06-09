---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [netscaler, snip, sta, certificates, storefront]
layer: rich
bron: inside-citrix-fma
---

# NetScaler SNIP, STA tickets and certificate practice

Bas explains a SNIP (Subnet IP) as best compared to a layer-3 routing table entry: it tells the NetScaler it has a connection to a specific network and how/where to reach it so it can route traffic there. A SNIP can also serve as a management IP alongside the NSIP.

On the Secure Ticket Authority (STA): it only applies when traffic traverses a NetScaler (external connections), so internal authentication needs no STA worries. The STA ticket is generated and sent back after a user launches an application/desktop — not during resource enumeration — and includes the resource to launch and the server to launch it on (load balance). The Broker (XML/STA) service must be configured identically, in the same load-balance/failover order, on both NetScaler and StoreFront.

Certificate best practice: use third-party certificates for external inbound connections and internal CA certificates for internal SSL traffic (e.g. StoreFront to Delivery Controllers); self-signed certificates are fine for test labs/PoCs.
