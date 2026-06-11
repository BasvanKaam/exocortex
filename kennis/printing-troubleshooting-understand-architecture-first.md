---
type: positie
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [printing, troubleshooting, citrix, philosophy]
bron: basvankaam-blog
---

# Tools are fine, but understand the architecture before you troubleshoot

In this Aug 2017 cheat sheet Bas argues that not much has actually changed in Citrix printing over the years: same delayed logons, crashing services, blue screens, CPU spikes, auto-create failures, and most still trace back to faulty print drivers and poorly designed print architectures. His position is that admins lean too hard on the many free troubleshooting tools and forget the basics. You need to understand the architecture (FMA components, the printing pathways, UPS/UPD setup and traffic flow), know how it behaves under normal conditions, assemble a personal toolkit and know where to find information 'in times of peace'. His framing: it isn't one thing, it's everything combined (endpoints, policies, physical placement of machines and printers) that makes or breaks a print architecture. Also: test drivers even when signed/Citrix-approved, prefer the UPD exclusively where possible, and apply isolation only where it makes sense.

*Bron: blogpost 'The ultimate Citrix printing internals cheat sheet - version 2.0' (2017-08-28), basvankaam.com.*

## Verwante notities

- [Bas's troubleshooting philosophy: prepare in times of peace](bas-troubleshooting-philosophy-prepare-in-peace.md)
- [The basics (almost) never change](basics-never-change-troubleshooting-philosophy.md)
- [Citrix client vs network printing pathway](citrix-client-vs-network-printing-pathway.md)
- [Citrix network vs client printing pathway](citrix-print-pathways-network-vs-client.md)
- [Citrix print troubleshooting tools](citrix-print-troubleshooting-tools.md)
- [Citrix Universal Print Server (UPS)](citrix-universal-print-server.md)
- [Never skip the basics: start troubleshooting at the event logs](never-skip-the-basics-event-logs.md)
- [Most Citrix printing pain is still bad drivers and bad architecture](positie-citrix-printing-still-driver-and-design-problem.md)
- [Print architecture is decided by all elements combined, not one knob](print-architecture-is-all-elements-combined.md)
- [Bas's print driver best practices](print-driver-best-practices.md)
- [Print driver isolation: None, Shared, Isolated](print-driver-isolation-modes.md)
- [Print-related troubleshooting tools (Print Detective, UPS Cert Tool, StressPrinters)](print-troubleshooting-tools.md)
- [Printing is the perennial pain admins shouldn't have to focus on](printing-is-a-perennial-euc-pain.md)
- [You can't troubleshoot what you don't understand](troubleshooting-know-the-basics.md)
