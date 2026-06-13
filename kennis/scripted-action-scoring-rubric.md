---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [hackathon, scripted-actions, review, rubric, powershell, nerdio, method]
layer: reference
gedateerd: nee
bron: nerdio-content
---

# Scripted-Action Review Rubric (Hackathon judging)

The scoring model I used to judge community scripted actions. Useful as a general quality bar for any PowerShell/automation script, not just contest entries. Panel members review independently of each other; the bigger the problem solved, the higher the score.

## Weighted criteria (points scale)
- 1-5: Script is easy to read, has a good description, clean use of code.
- 1-5: Original approach to a challenge, an idea not seen before.
- 1-10: Script runs without errors and achieves the desired outcome / solves the challenge.
- 1-15: Script contains error checking and validation.
- 1-20: Script uses native APIs where possible instead of depending on other modules or libraries.
- 1-25: Script integrates into other systems to achieve the outcome (e.g. Ansible, CI/CD pipelines).

## What the weighting says about good automation
The escalating point values encode a philosophy: correctness and readability are table stakes; the real value is in robustness (error checking/validation), minimizing dependencies (native APIs over external modules), and composing into larger systems (pipelines, integrations). Originality is rewarded but capped low compared to engineering rigor.

## Judging conduct
- Reviewers must be able to run the script; if it cannot be executed, no points are assigned, and the author is contacted to validate the issue.
- No formal plagiarism check unless obvious; fair play is assumed. Reusing your own code is fine.
- All authors credited at the top of their scripts.

*Bron: Nerdio-content 'Hackathon overview doc.docx' (Hackathon).*

## Verwante notities

- [Idea: Community Scripted Actions Hackathon](idee-nerdio-scripted-actions-hackathon.md)
