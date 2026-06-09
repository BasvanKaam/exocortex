---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [citrix, netscaler, nsip, snip, mip, networking]
layer: reference
bron: inside-citrix-fma
---

# NetScaler IP addresses: NSIP, SNIP and MIP

**NSIP (NetScaler IP / Management IP):** the address an administrator uses to manage and configure the NetScaler. Mandatory on first setup, there can be only one, it cannot be removed, and changing it requires a reboot.

**SNIP (Subnet IP):** used for server-side connections, routing traffic from/through the NetScaler to a directly connected subnet. The default **USNIP (Use SNIP)** mode makes the SNIP the source address for packets sent to the internal network. Configuring a SNIP adds a corresponding route to the NetScaler's routing table (best compared to a layer-3 routing table entry). A SNIP is not mandatory; in multi-subnet scenarios you configure one per subnet, and multiple SNIPs on the same subnet are used round-robin. By default a SNIP isn't bound to a specific interface — traffic goes out on all interfaces (closer to a hub) — but it can be bound to one or more interfaces.

**MIP (Mapped IP):** comes into play when USNIP is disabled or no SNIP is available, acting as the source IP. When a MIP and SNIP share a subnet, the MIP may also be used as source IP, but only if the MIP is the first address on the subnet does a route get added to the routing table.

**Default route:** functions as the NetScaler's default gateway; without known internal routes (SNIP/MIP) it sends all traffic back out the default route. **Net profiles** (optional) predefine which SNIP to use for back-end communication, which simplifies firewall ACL rules.
