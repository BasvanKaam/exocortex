---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [windows-10, waas, servicing-branches, deployment-rings, sccm, wsus, patching]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Windows 10 servicing branches and deployment rings

How Windows-as-a-Service (WaaS) worked in the original Windows 10 servicing model (2016, before the later SAC/SAC-T rename):

Update types:
- Feature updates: new functionality and features, delivered 2-3 times per year (replacing the old every-3-to-5-years full Windows release).
- Quality updates: security fixes/patches and other less-vital updates, delivered at least monthly (Patch Tuesday) as a single cumulative monthly update so all machines end up equally patched.

Three servicing branches (deployment groups):
- Current Branch (CB): feature updates available as soon as Microsoft releases them. For dev/IT/PoC/pilot/test machines.
- Current Branch for Business (CBB): same bits as CB but transferred ~4 months later, after an extra round of testing. For company-wide deployment.
- Long-Term Servicing Branch (LTSB): no feature updates ever, only quality updates. New LTSB releases roughly every 2-3 years, over a 10-year lifecycle. For highly secure, business-critical systems that shouldn't change.
- All branches get quality updates instantly, and (depending on Win10 version 1511 vs 1607+ and tooling) can defer feature/quality updates from 30 days up to eight months.

Deployment rings just separate machines into a deployment timeline within/across branches; the concept is consistent though configuration differs per tool.

Tooling: Windows Update (not really enterprise-worthy), SCCM, WSUS, and the then-new Windows Update for Business. Existing tools still apply; no need to switch.

*Bron: blogpost 'Windows 10 servicing branches, deployment rings and update tooling' (2016-11-14), basvankaam.com.*

## Verwante notities

- [Citrix LTSR vs CR servicing model](citrix-ltsr-vs-cr-servicing.md)
- [LTSR is the right call, but not for everybody](ltsr-is-not-for-everybody.md)
- [After disruptive patches, measure impact per workload instead of guessing](measure-dont-guess-capacity-after-patches.md)
- [Meltdown/Spectre patches carried a real performance cost - patch anyway](meltdown-spectre-patch-performance-cost.md)
- [ProPlus deployment and update tooling options](o365-proplus-deployment-and-update-options.md)
- [Office 365 ProPlus Update Channels model](o365-update-channels-model.md)
- [ProPlus channel freedom of choice (ring deployment)](office-365-proplus-channel-freedom-of-choice.md)
- [Office 365 ProPlus update channels](office-365-proplus-update-channels.md)
- [Office vs Office 365 vs Office 365 ProPlus: what is what](office-vs-office365-vs-proplus.md)
- [OS Migration Is More Than Swapping the OS](os-migration-is-more-than-the-os.md)
- [Organizations want control over updates, not full automation](position-control-updates-dont-fully-automate.md)
- [Test quality updates, not just feature updates](test-quality-updates-too.md)
- [Windows 10 was never the promised 'One OS to rule them all'](windows-10-not-one-os-to-rule-them-all.md)
- [Windows SAC vs LTSC servicing channels](windows-sac-vs-ltsc-servicing-channels.md)
- [Windows Server 2019 at announcement: LTSC/SAC, RDSH question, RDmi](windows-server-2019-ltsc-sac-rdmi.md)
- [Windows user profile versions are incompatible across OS releases](windows-user-profile-version-incompatibility.md)
