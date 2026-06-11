---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [office-365, non-persistent, vdi, outlook-ost, user-profile]
layer: reference
gedateerd: nee
bron: basvankaam-blog
---

# Office 365 cached-mode OST files break on non-persistent desktops

Office 365 / Outlook runs in online mode (live connection to Exchange Online, needs low-latency link, performance often poor) or cached mode (Microsoft-recommended), where a local copy of the mailbox and Offline Address Book is stored in an .OST file under C:\Users\<user>\AppData\Local\Microsoft\Outlook.

On non-persistent VDI/RDSH the user is randomly assigned a fresh desktop each logon and the session is discarded at logoff, deleting locally stored data including the OST. Keeping the OST inside the roaming profile instead bloats the profile heavily and slows every login as it reloads onto each new machine. This OST-on-non-persistent problem is a core driver for profile-container technologies (ProfileDisk / FSLogix-style VHD containers).

*Bron: blogpost 'The Easy Button - Corruption, Portability, Office 365, User Profile bloat, ProfileDisk, non-persistent Data Indexing and more' (2018-01-14), basvankaam.com.*

## Verwante notities

- [Citrix's native options still lag third-party containers (May 2018)](citrix-still-behind-third-party-containers-2018.md)
- [Citrix WEM/UPM per-user Outlook search + OST roaming (Synergy 2018)](citrix-wem-upm-ost-search-roaming-2018.md)
- [Delivering Lync in a XenApp hosted shared desktop: generic vs optimized HDX](lync-xenapp-delivery-options.md)
- [The non-persistent Office 365 / Outlook OST and search-index problem](non-persistent-outlook-search-ost-problem.md)
- [Office 365 cached mode breaks on non-persistent VDI/RDSH](office365-cached-mode-nonpersistent-problem.md)
- [Office 365 pain on non-persistent VDI, solved by containers](office365-nonpersistent-vdi-fslogix.md)
