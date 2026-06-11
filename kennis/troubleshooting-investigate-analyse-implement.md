---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [troubleshooting, methodology, efficiency]
layer: rich
bron: inside-citrix-fma
---

# Investigate, Analyse, Implement: Bas's structured troubleshooting approach

Bas frames troubleshooting as being all about efficiency: fixing an issue should take as little time as possible, which calls for a structured methodology he names Investigate, Analyse and Implement.

His sequence:
- First, acknowledge there actually is a problem, and consider your source (helpdesk, the CEO, a chronic complainer).
- Find out what the actual issue is: how many users or departments are affected, and how do they describe it? Talk to users and the Helpdesk.
- Assess overall business impact: are business-critical systems or processes involved? For a potential major outage, estimate the time and resources needed for a fix, even a temporary one. Can the problem be reproduced?
- Isolate the issue: which components/services are actually affected? Plan accordingly.
- Check event logs (a Doctor Watson log perhaps), monitoring software, and any recent changes to the environment. Studio/Director can help. A simple PING or Tracert might tell you something.

His core advice: start small, take the relatively 'easy' steps first, try to make progress, and look for quick fixes or workarounds.

## Verwante notities

- [Bas's troubleshooting philosophy: prepare in times of peace](bas-troubleshooting-philosophy-prepare-in-peace.md)
- [Citrix Director: monitoring and troubleshooting tool](citrix-director-overview.md)
- [Domain Controller Health-Check CLI Routine](dc-health-check-cli-routine.md)
- [Don't forget old-school tools (NetStat, Ping, Tracert, Telnet)](old-school-troubleshooting-tools.md)
- [Terminal Server / Citrix troubleshooting checklist (own notes)](terminal-server-troubleshooting-checklist.md)
- [Bas's troubleshooting and sizing philosophy](troubleshooting-and-sizing-philosophy.md)
- [Bas's general troubleshooting tips (facts, not guesses)](troubleshooting-general-tips-bas.md)
- [Bas's troubleshooting philosophy: master the basics before reaching for tools](troubleshooting-know-the-basics-first.md)
