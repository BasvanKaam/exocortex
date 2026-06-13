---
type: positie
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [euc, wvd, avd, operations, risk, positie]
bron: nerdio-blog
---

# Don't put all your eggs in one basket: knowledge as a single point of failure

Bas argues that relying on a few senior, script-heavy admins to run WVD/AVD creates a knowledge single point of failure. His chain of reasoning:

- The senior 20% can automate, script image updates and run DevOps-style deployments smoothly, until something breaks and they are unavailable: time off, long-term illness, or they leave the company.
- Training other employees doesn't fix it cleanly. Doing the job because you're told to is different from doing it out of passion, and not everyone wants that responsibility.
- Hiring expertise in is costly, the hire won't know your company the way the departed employee did, and they will eventually leave too. A vicious circle.

His conclusion: the goal is to relieve individuals from unneeded stress, spread workload evenly, do more with less, and remove the single point of failure by making setup/management simple enough (via better tooling, in his case Nerdio) that 80%+ of technical staff can stand in for each other and set up/manage WVD within hours, with no steep learning curve and no PowerShell/ARM/JSON requirement (while still supporting scripting for those who want it).

*Bron: Nerdio-content 'Notes From the Field (CTO) – the July 2020 edition' (Blogs).*

## Verwante notities

- [Be realistic about automation as a business](automation-realistic-business-view.md)
- [The real win of WVD automation is reclaimed admin time, not just compute](automation-saves-time-equals-money-position.md)
- [Bas: IaC Creates Dangerous Key-Person Dependency](bas-iac-key-person-risk.md)
- [Idea: Bridge! - A Structured Internal Mentoring Program](idea-bridge-mentoring-program.md)
- [Key-person dependency on automation is a business risk](key-person-dependency-as-business-risk.md)
- [Concentrated cloud knowledge in a few seniors is a business risk](knowledge-leaving-the-company-as-a-real-risk.md)
- [Support is a Differentiator, Not an Afterthought](support-as-a-differentiator-nerdio.md)
- [The 80/20 'two kinds of sysadmin' framework](two-kinds-of-sysadmin-80-20.md)
