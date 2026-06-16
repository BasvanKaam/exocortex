---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [liquidware, profileunity, flexapp, application-layering, uem, vhd, vmdk]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# FlexApp 6.5: filter drivers replace symbolic links, broadening layering support

How Liquidware ProfileUnity / FlexApp worked at version 6.5 (late 2015).

ProfileUnity is a complete UEM solution including FlexApp application layering, managed from a single web-based console (the two products can also be bought separately).

Key 6.5 change: prior to 6.5, FlexApp layered apps relied on symbolic links, so they only worked for virtual non-persistent machines and could only be assigned per user/group. As of 6.5 FlexApp uses file-system filter drivers instead, so layered apps look native to the OS and can interact with locally installed apps, and now work for virtual and physical, non-persistent and persistent desktops. Assignment is still per user/group, plus 300+ context-aware filters.

Packaging: run the FlexApp Packaging Console on a non-persistent VM; install/registry changes are redirected and saved to a VHD or VMDK.

Profiles: as of 6.5 user profiles can also be stored in VHD/VMDK and mounted like a FlexApp layer. This limits SMB traffic to reads and writes (similar in spirit to FSLogix, not identical) versus a constant stream with traditional folder redirection. Profiles can roam across Windows versions (from XP upward).

Flavours/scope: VHD (mounted in-guest, works on virtual and physical) and VMDK for VMware (mounted at hypervisor level, virtual only). Works with XenApp, RDSH, XenDesktop, VMware View and physical machines. Config/policy data is stored by default in the domain NetLogon share (INI files, small, cached locally for offline use); actual VHD/VMDK and profile data live wherever you choose. Important: this is application layering, not application virtualisation (no isolation like ThinApp/App-V); layering is often used in conjunction with app virtualisation.

*Bron: blogpost 'Liquidware ProfileUnity & FlexApp 6.5 overview' (2015-09-12), basvankaam.com.*

## Verwante notities

- [Application layering: abstract the app from the OS](app-layering-abstraction-durable-concept.md)
- [In-guest vs hypervisor-level mounting in application layering](app-layering-in-guest-mounting-explained.md)
- [Framing: keep application layering and application virtualization distinct](app-layering-not-app-virtualization.md)
- [Citrix App Layering's reputation problem (2018)](citrix-app-layering-reputation-2018.md)
- [How application layering works (filter drivers)](how-application-layering-works.md)
- [Liquidware suite: ProfileUnity, FlexApp, Stratusphere UX (2018)](liquidware-profileunity-flexapp-stratusphere.md)
- [ProfileDisk: redirect the whole profile to a VHD/VMDK container](profiledisk-container-concept.md)
- [ProfileUnity feature set and all-in-one model (2017)](profileunity-feature-overview-2017.md)
