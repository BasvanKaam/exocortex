---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [office-365, proplus, update-channels, deployment, whitepaper]
layer: reference
gedateerd: ja
bron: salomon-whitepaper
---

# Office 365 ProPlus Update Channels model

From the 2019 whitepaper. After picking a subscription and plan, an organization chooses an Update Channel: think of it as groups of users where one group receives new functionality before another (for testing before production rollout).

Three channels:
- Monthly Channel: users get the newest features immediately, generally monthly.
- Semi-Annual Channel: new features twice a year, January and July. This is the ProPlus default.
- Semi-Annual Channel (Targeted): for pilot users and compatibility testers; features in March and September, four months ahead of the regular Semi-Annual release, so issues surface early.

Security and quality updates ship monthly for every channel regardless. Each ProPlus update is effectively a new Office version and is supported for a maximum of 18 months. The Targeted support clock starts at the Targeted release (e.g. March), so by the time it becomes the regular Semi-Annual release (July), four of the eighteen months are already spent, leaving fourteen.

You switch channels via the Office Deployment Tool or Group Policy (config.office.com).

Time-bound: this channel naming and cadence is the 2019 scheme.

*Bron: Salomon-IT 'Whitepaper'.*

## Verwante notities

- [ProPlus deployment and update tooling options](o365-proplus-deployment-and-update-options.md)
- [Office 365 ProPlus versus traditional Office](o365-proplus-vs-traditional-office.md)
- [ProPlus channel freedom of choice (ring deployment)](office-365-proplus-channel-freedom-of-choice.md)
- [Office 365 ProPlus update channels](office-365-proplus-update-channels.md)
- [Organizations want control over updates, not full automation](position-control-updates-dont-fully-automate.md)
- [Windows 10 servicing branches and deployment rings](windows10-servicing-branches-rings.md)
