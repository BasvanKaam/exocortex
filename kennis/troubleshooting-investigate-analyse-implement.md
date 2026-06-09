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
