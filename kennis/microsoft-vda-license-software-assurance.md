---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-09
tags: [microsoft, vda, software-assurance, vdi, licensing]
layer: reference
bron: inside-citrix-fma
---

# Microsoft VDA licenses and Software Assurance

**VDA = Virtual Desktop Access.** Every Windows and non-Windows device accessing a Windows desktop OS based VM (VDI only) must be licensed with a Microsoft VDA license. If corporate Windows PCs are covered by Microsoft **Software Assurance (SA)** or Windows Intune, VDA rights are automatically included, so no separate VDA purchase is needed. Buying VDA separately is optional and especially relevant for smaller companies that can't afford SA. A standalone VDA license costs about **$100 per year, per device**.

Exception: non-Windows machines such as Linux thin clients still need separate VDA licenses. Technically SA is an upgrade of an existing (usually OEM) license, which is why thin clients can't carry SA — there's no existing license to upgrade — and need VDA instead.

**Roaming rights:** a user with a corporate VDA-licensed device may use their home PC to access the corporate VM under the same VDA license, but a personally owned non-corporate device brought into the office needs its own VDA license. Per Microsoft, roaming rights only apply while roaming outside the corporate domain.

Important scope: VDA licenses do not apply to Citrix XenApp — if you access a Windows desktop OS VM from a physical PC (not on a server), no VDA license is needed. SA benefits allow up to four VMs (VDI) or one physical machine running a Windows desktop OS.
