---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [deployment, prerequisites, method, consulting, xenmobile]
layer: reference
gedateerd: nee
bron: basvankaam-blog
---

# Inspecting prerequisites up front saves the whole deployment

A durable consulting principle Bas hammers: don't underestimate prerequisites. Pre-inspecting the prerequisites (firewall ports/protocols, IPs, DNS, AD, certificates, authentication, hardware/software, licensing) up front does two things: it tells you whether you have what it takes, and it saves significant time once you start building.

Two concrete, still-relevant lessons from the XenMobile context:
- Start the slow dependencies early. Opening firewall ports is a 2-minute job, but in practice can take days because networking teams are 'known' for that. Make it a high-priority item and involve the network team as soon as possible.
- Names and addresses must be resolvable before you install. Inventory FQDNs/IPs of database, NetScaler (NSIP/SNIP/VIP), AD, DNS, NTP, SMTP, etc. in advance; if they aren't up and resolvable, you get stuck mid-install.

The product is dated, but the prerequisites-first discipline and 'start the slow stuff early' rule are durable.

*Bron: blogpost 'XenMobile prerequisits, what do we need and how does it all fit together?' (2014-05-12), basvankaam.com.*

## Verwante notities

- [The basics (almost) never change](basics-never-change-troubleshooting-philosophy.md)
- [Troubleshooting tip #1: document what you've done](document-your-troubleshooting.md)
- [DSC prerequisites: WMF / PowerShell 4.0 on every machine involved](dsc-prerequisites-wmf4.md)
- [WVD prerequisites Nerdio still relies on: AD sync and FSLogix profiles](nerdio-wvd-prerequisites-ad-fslogix.md)
- [NetScaler IP terminology: NSIP, SNIP, MIP, VIP, vServer](netscaler-ip-terminology.md)
- [Never skip the basics: start troubleshooting at the event logs](never-skip-the-basics-event-logs.md)
- [In a PoC the software is easy, the environment is the hard part](poc-setup-the-hard-part-is-the-environment.md)
- [Reboots are a necessary evil; handle them proactively](proactive-over-reactive-ops.md)
- [Server 2012 .NET 3.5 Feature on Demand install gotcha (how it worked then)](server-2012-net35-feature-on-demand-gotcha.md)
- [You can't troubleshoot what you don't understand](troubleshooting-know-the-basics.md)
- [XenMobile is hard to deploy even when you know what you're doing](xenmobile-complex-even-if-you-know-how.md)
- [XenMobile MDM moved off the DMZ via NetScaler SSL offloading](xenmobile-ssl-offloading-netscaler.md)
