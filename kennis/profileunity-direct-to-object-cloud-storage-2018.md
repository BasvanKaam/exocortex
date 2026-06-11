---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [liquidware, profileunity, flexapp, s3, azure-blob, gcs, cloud-storage, uem]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# ProfileUnity saving direct to object cloud storage (no SMB file shares)

How it worked then (mid-2018, ProU/FA v6.7.7.6701): Liquidware ProfileUnity added the ability to save configuration files, license file and portability data directly to object-based cloud storage, removing the need for traditional SMB file shares. Amazon S3 came first (April 2018), then Azure Blob Storage and Google Cloud Storage in the weeks after, each aimed at desktops/RDS running on the matching cloud (Amazon Workspaces/EC2, Azure, GCP). FlexApp (which tightly integrates with ProfileUnity and is managed from the same console) was announced to get the same direct-to-object-storage support.

The durable concept underneath: profiles, policy data and application layers can roam against block/object cloud storage APIs instead of requiring an SMB file-server infrastructure, the key enabler for hybrid on-prem/cloud workspace portability. Other 6.7-era improvements worth noting: faster logins using the Windows local token for group membership (instead of querying AD), WMI repair/preload on boot, faster VHD unmounts, and Windows 10 modern-app pin/delete support for tiles and taskbar.

*Bron: blogpost 'Innovation and making progress! Liquidware - you've heard about them before, right?' (2018-06-03), basvankaam.com.*

## Verwante notities

- [FSLogix Cloud Cache (tech preview, 2018)](fslogix-cloud-cache-2018.md)
- [The Liquidware portfolio in 2017: Stratusphere, ProfileUnity, FlexApp](liquidware-portfolio-2017.md)
- [Liquidware suite: ProfileUnity, FlexApp, Stratusphere UX (2018)](liquidware-profileunity-flexapp-stratusphere.md)
- [Use one UEM layer across physical, virtual, on-prem and cloud](one-uem-layer-across-physical-virtual-cloud.md)
- [ProfileDisk: redirect the whole profile to a VHD/VMDK container](profiledisk-container-concept.md)
- [ProfileUnity feature set and all-in-one model (2017)](profileunity-feature-overview-2017.md)
