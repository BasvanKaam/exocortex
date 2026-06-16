---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-11
tags: [onedrive, migration, sharegate, powershell, modern-workplace, office-365, guest-post]
layer: reference
gedateerd: ja
bron: cgit-blog
---

# Migrating homefolders and profiles to OneDrive with ShareGate

Author: Niels Kok (guest post on the CGIT blog). Not Bas van Kaam's voice — captured for the durable method only.

The modern workplace conversation tends to focus on functional value; this is the technical how-to for moving profiles and homefolders to OneDrive. Online guidance is fragmented; ShareGate is used as the third-party tooling to automate and script the migration.

Step-by-step method:
1. Inventory the data. Which folders must be excluded? Are there multiple sources (profiles and homefolders)? Build a clear overview of what lives where, how much there is, and where it must land.
2. Assign licenses to users first. Unlike Exchange Online, you cannot sync first and assign the license later. No license, no migration.
3. Provision the OneDrives. A license does not auto-create the OneDrive (again unlike Exchange Online). The user must log in once to provision it — or you bulk pre-provision via PowerShell with the SharePoint Online module (`Request-SPOPersonalSite -UserEmails ... -NoWait`). Pre-provisioning requests go into a queue and typically complete after about an hour; the script finishing does not mean every OneDrive is ready.
4. Grant migration rights across every OneDrive in the tenant. Use a generic/neutral admin account so users do not get suspicious about someone having access to their OneDrive. Use ShareGate's report function to enumerate all OneDrives, then assign rights. Steps 2 and 3 must be complete or this fails.
5. Build a mapping CSV with DIRECTORY;ONEDRIVEURL so source path and OneDrive URL are known to the script. Personal site URL format: `https://tenant-my.sharepoint.com/personal/username_domain_nl/` (replace `@domain.nl` with `_domain_nl/`). A recursive `Get-ChildItemToDepth` PowerShell function is offered to enumerate homefolders/profiles into the CSV.
6. Run the ShareGate migration script to upload everything to OneDrive.

Scale note: the author ran this for ~1100 users.

*Bron: Salomon-IT 'Niels_ComeGetITBlog' (CGIT Blogs).*

## Verwante notities

- [Baseline Criteria for Modern App and Desktop Delivery (anno 2020)](modern-workplace-delivery-baseline-2020.md)
- [Office 365 Network Performance: Service Front Doors and the Basics](office365-network-performance-basics.md)
- [Office 365 on VDI/RDSH: .OST Bloat and the Search-Index Problem](office365-profile-pain-ost-and-search-index.md)
- [Profile Layering with FSLogix: Mount Instead of Copy](profile-layering-fslogix.md)
- [User Profiles on VDI/RDSH: Bloat, Corruption and Roaming Challenges](user-profiles-roaming-challenges.md)
