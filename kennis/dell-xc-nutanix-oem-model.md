---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-10
tags: [nutanix, dell, hyper-converged, oem, web-scale]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Dell XC series: same Nutanix software, different hardware

How it worked then (Nov 2014): Following a June 2014 OEM agreement, Dell shipped the XC series, web-scale converged appliances running Nutanix software on Dell PowerEdge R720-based hardware (2U nodes, versus four Nutanix nodes per 2U appliance). Key point Bas emphasizes: Nutanix changed nothing about its software. A Dell node and a Nutanix node run the same NOS versions, get the same updates, and are managed through the same Prism UI; only the underlying hardware differs. The one exception: KVM was not supported on Dell nodes (choice of ESXi or Hyper-V, pre-installed before delivery). Minimum three nodes to form a cluster; up and running in 30-60 minutes including HA. Support was joint Dell+Nutanix via a single number, led by Dell. Dated product specifics, but a clean illustration of the OEM 'same software, partner hardware' pattern.

*Bron: blogpost 'Powered by Nutanix! Check out the new Dell hyper-converged XC series!' (2014-11-05), basvankaam.com.*

## Verwante notities

- [What a converged infrastructure is](converged-infrastructure-definition.md)
- [Nutanix-Dell OEM agreement and the Dell XC appliance line (2014)](nutanix-dell-oem-xc-2014.md)
- [Nutanix is a mature product and here to stay](nutanix-here-to-stay-2014.md)
- [How Nutanix NOS 4.0 worked: Prism Central, integrated data protection, one-click upgrade](nutanix-nos-4-features-2014.md)
- [OEM deals will democratize web-scale infrastructure](web-scale-for-everyone-prediction.md)
