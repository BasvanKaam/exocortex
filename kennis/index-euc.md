---
type: index
merk: bvk
domein: euc
status: actief
datum: 2026-06-15
tags: [index, navigatie, euc]
---

# euc - index

Map of Bas van Kaam's end-user computing knowledge: Citrix FMA, AVD/WVD, Windows 365, app delivery, profiles, printing, NetScaler, storage and the community positions that run through it all. Hub notes (most-linked) lead each section.

## Citrix FMA architecture
- [The Delivery Controller as the heart of the FMA](delivery-controller-heart-of-fma.md)
- [Excalibur merges XenApp and XenDesktop onto FMA](excalibur-merges-xenapp-xendesktop-fma.md)
- [The evolution of the FlexCast Management Architecture](evolution-of-the-fma.md)
- [The FlexCast Management Architecture and its thirteen core services](fma-thirteen-core-services-overview.md)
- [Delivery Controller vs Data Collector differences](delivery-controller-vs-data-collector.md)
- [FMA Zones: architecture and purpose](fma-zones-architecture-and-purpose.md)
- [How Local Host Cache works in the FMA](local-host-cache-712-architecture.md)
- [Connection Leasing mechanism](connection-leasing-mechanism.md)
- [Broker Service: XML, STA and the Principal Broker](broker-service-xml-sta-principal.md)
- [Zones in the FMA are not the same as IMA 6.5 Zones](zones-fma-vs-ima.md)
- [Citrix Studio: the central management console](citrix-studio-overview.md)
- [Machine Catalogs and Delivery Groups: mixed-OS flexibility](catalogs-delivery-groups-mixed-os.md)
- [High-availability options for the Central Site database](central-site-database-ha-options.md)
- [Citrix LTSR vs CR servicing model](citrix-ltsr-vs-cr-servicing.md)
- [The origin of Citrix and the ICA protocol](history-of-citrix-and-ica.md)

## VDI, DaaS and image management
- [DaaS versus VDI](daas-vs-vdi.md)
- [Single-User vs Multi-User VDI/DaaS](single-user-vs-multi-user-vdi-daas.md)
- [The 'big bad image' problem: why everything in the base image hurts](big-bad-base-image-problems.md)
- [Pooled vs dedicated desktops: the durable trade-off](pooled-vs-dedicated-desktops.md)
- [The five VDI workload phases and boot/logon storms](vdi-five-phases-storms.md)
- [Citrix Provisioning Services (PVS) overview](provisioning-services-overview.md)
- [Machine Creation Services (MCS): integrated single-image delivery](machine-creation-services-overview.md)
- [How Citrix MCS provisions VMs: snapshot, differencing disk, identity disk](mcs-how-it-works-disks.md)
- [MCS desktop types: pooled-random, pooled-static, dedicated](mcs-desktop-types-pooled-dedicated.md)
- [MCS planning: master-VM count x data-store count x update frequency](mcs-storage-and-update-cycle-cost.md)
- [PVS write cache options](pvs-write-cache-options.md)
- [PVS high availability](pvs-high-availability.md)
- [Personal vDisks (PvD)](pvs-personal-vdisks-pvd.md)
- [VIAB vs XenDesktop: simplicity vs flexibility tradeoffs (2013)](viab-vs-xendesktop-tradeoffs.md)

## AVD / Windows Virtual Desktop
- [Windows Virtual Desktop: multi-user Windows 10 as DaaS on Azure](wvd-multi-user-windows10-daas-2019.md)
- [From Terminal Services to AVD - The Multi-User History](history-terminal-services-to-avd.md)
- [Early WVD architecture: Microsoft-managed PaaS control plane + reverse connect](early-wvd-architecture-control-plane.md)
- [WVD is what used to be RDMI](wvd-is-rdmi-on-prem-history.md)
- [WVD introduced multi-user Windows 10 and a license-based entitlement model](wvd-win10-multiuser-and-licensing.md)
- [How Windows 10 multi-session came to light (2018)](windows-10-multi-session-origins-2018.md)
- [AVD - The Only Cloud Service That Runs Windows Client Multi-User](avd-windows-client-multi-user.md)
- [WVD hit general availability on September 30, 2019](wvd-ga-date-sept-2019.md)
- [WVD roadmap signals from the 2019 workshop](wvd-roadmap-signals-2019.md)
- [Common WVD/Azure adoption challenges (from the field)](common-wvd-adoption-challenges.md)
- [WVD is not a click-and-go product](wvd-not-click-and-go.md)
- [Bas's reframe: is AVD and/or Windows 365 Cloud PC really DaaS?](is-avd-and-windows-365-really-daas.md)

## Windows 365 / Cloud PC
- [Windows 365 Cloud PC](windows-365-cloud-pc.md)
- [Windows 365 Cloud PC - Business vs Enterprise](windows-365-business-vs-enterprise.md)
- [Windows 365 Cloud PC - Pros, Cons and Cost Control vs AVD](windows-365-pros-cons.md)
- [Windows in the cloud as a living persona](windows-in-the-cloud-as-living-persona.md)
- [Why cloud DaaS ran on Server OS, not client OS (the licensing trap)](daas-licensing-server-os-workaround.md)
- [Citrix Managed Desktop: single-bill DaaS on Citrix-managed Azure](citrix-managed-desktop-model-2019.md)

## App delivery, layering and virtualization
- [Application layering: abstract the app from the OS](app-layering-abstraction-durable-concept.md)
- [Application layering complements, does not replace, app virtualization](application-layering-vs-virtualization.md)
- [Application virtualisation tops out around 70-80% in practice](app-virtualisation-ceiling-70-80.md)
- [Three flavours of application delivery in XenDesktop/XenApp](application-delivery-three-flavours.md)
- [Citrix acquired Unidesk to own application layering](citrix-acquires-unidesk-layering.md)
- [Application layering vendor landscape circa 2016](application-layering-vendor-landscape-2016.md)
- [MSIX app attach: VHD-mounted apps via FSLogix filter drivers](msix-app-attach-concept.md)
- [MSIX positioned to replace App-V (2019 transition)](msix-replacing-app-v.md)
- [Microsoft App-V components and licensing with Citrix](microsoft-app-v-with-citrix.md)
- [How application layering works](how-application-layering-works.md)

## User profiles, FSLogix and UEM
- [Liquidware suite: ProfileUnity, FlexApp, Stratusphere UX (2018)](liquidware-profileunity-flexapp-stratusphere.md)
- [FSLogix Profile Containers as the WVD profile standard (2019)](wvd-profiles-fslogix-azure-files-2019.md)
- [FSLogix Cloud Cache (tech preview, 2018)](fslogix-cloud-cache-2018.md)
- [Profile Portability: an abstraction layer over the user profile](profile-portability-abstraction-engine.md)
- [Hybrid user profiles vs roaming profiles](hybrid-user-profiles-explained.md)
- [How a Windows user profile loads](windows-roaming-profile-loading.md)
- [Office 365 pain on non-persistent VDI, solved by containers](office365-nonpersistent-vdi-fslogix.md)
- [The non-persistent Office 365 / Outlook OST and search-index problem](non-persistent-outlook-search-ost-problem.md)
- [The Liquidware portfolio in 2017: Stratusphere, ProfileUnity, FlexApp](liquidware-portfolio-2017.md)
- [RES PowerFuse / Workspace Manager (reference)](res-powerfuse-workspace-manager-overview.md)

## StoreFront, Receiver and HDX
- [StoreFront 2.0 replaces Web Interface (key features)](storefront-2-replaces-web-interface.md)
- [StoreFront authentication and resource enumeration traffic flow](storefront-authentication-traffic-flow.md)
- [StoreFront Multi-Site aggregation, mapping and failover](storefront-multisite-aggregation.md)
- [Three ways to reach resources via Receiver, including HTML5 clientless access](receiver-three-ways-and-html5-clientless.md)
- [Citrix Receiver: purpose and naming history](citrix-receiver-history-and-purpose.md)
- [Configuring Receiver connection information](receiver-connection-configuration-methods.md)
- [Citrix HDX display codecs and their confusing alternate names](citrix-hdx-display-codecs-overview.md)
- [Citrix HDX: an extension to ICA, not a replacement](citrix-hdx-extends-ica.md)
- [ThinWire compatibility mode: the low-footprint fallback for H.264](thinwire-compatibility-mode.md)
- [What the ICA protocol does and its default ports](ica-protocol-fundamentals.md)
- [ICA virtual channels: 32 total, 17 reserved by Citrix](ica-virtual-channels.md)
- [Framehawk: ICA over lossy, high-latency networks](framehawk.md)
- [Citrix Adaptive Transport (Enlightened Data Transport / EDT)](citrix-adaptive-transport-edt.md)

## NetScaler / networking
- [External user authentication through NetScaler](external-authentication-through-netscaler.md)
- [NetScaler Gateway remote-access traffic flow](netscaler-gateway-traffic-flow.md)
- [NetScaler IP terminology: NSIP, SNIP, MIP, VIP, vServer](netscaler-ip-terminology.md)
- [NetScaler SSL offloading and DMZ placement](netscaler-ssl-offload-dmz.md)
- [NetScaler HA pair: heartbeats, failover and config replication](netscaler-ha-pair-fundamentals.md)
- [NetScaler binding chain: virtual server to service to server object](netscaler-virtual-service-server-objects.md)
- [NetScaler Unified Gateway](netscaler-unified-gateway.md)
- [NetScaler edition licenses and Pay-as-you-Grow](netscaler-adc-edition-licenses-pay-as-you-grow.md)
- [External launch process: Hosted Shared Desktop via NetScaler](external-launch-process-hsd-netscaler.md)
- [DNS resource record types](dns-resource-record-types.md)

## Printing
- [Citrix Print Management Service](citrix-print-management-service.md)
- [Citrix printing pathways: client vs network](citrix-printing-pathways-client-vs-network.md)
- [Citrix Universal Print Driver (UPD)](citrix-universal-print-driver.md)
- [Citrix Universal Print Server (UPS)](citrix-universal-print-server.md)
- [Print architecture is decided by all elements combined, not one knob](print-architecture-is-all-elements-combined.md)
- [Bas's checklist to speed up and clean up Citrix printing](bas-citrix-printing-optimization-checklist.md)
- [Bas's print driver best practices](print-driver-best-practices.md)
- [Print driver versions and Print Driver Isolation](print-driver-history-and-modes.md)
- [Print spooling: local vs remote](print-spooling-local-vs-remote.md)
- [Citrix proximity printing](citrix-proximity-printing.md)

## Monitoring, troubleshooting and sizing
- [Citrix Scout: the aggregating troubleshooting tool](citrix-scout-aggregator.md)
- [Citrix Insight Services: automated log analysis and health checks](citrix-insight-services.md)
- [Director and built-in EdgeSight](director-monitoring-tool.md)
- [Citrix Director: monitoring and troubleshooting tool](citrix-director-overview.md)
- [The Citrix XenDesktop/XenApp 7.x troubleshooting toolset](citrix-7x-troubleshooting-toolset.md)
- [Login VSI and VSImax: benchmarking by saturation](loginvsi-vsimax-saturation-benchmark.md)
- [VDI Drones: synthetic load testing without user accounts (2018)](vdi-drones-synthetic-load-testing.md)
- [Bas on IOPS, latency and storage sizing](iops-and-latency-fundamentals.md)
- [Bas on sizing: there is no 'one size fits all', and don't overdo it](sizing-no-one-size-fits-all.md)
- [Go-EUC: independent community EUC performance research](go-euc-performance-research-platform.md)

## Storage and infrastructure
- [Block vs file level storage: the durable trade-off](block-vs-file-level-storage.md)
- [Why traditional SANs are complex for virtual workloads](traditional-san-complexity.md)
- [IOPS, latency, and sizing storage for VDI workloads](iops-latency-and-sizing-storage-for-vdi.md)
- [Not all IOPS are the same: the three golden parameters](iops-not-all-the-same.md)
- [What a converged infrastructure is](converged-infrastructure-definition.md)
- [Nutanix Acropolis is three components, not just a hypervisor](nutanix-acropolis-three-components.md)
- [VMware instant clones / VMFork mechanics](vmware-instant-clones-vmfork-mechanics.md)

## Mobility, BYOD and endpoints
- [2013 mobile management vendor landscape](byod-vendor-landscape-2013.md)
- [Mobile management acronyms: MDM, MAM, MIM, EMM](mdm-mam-mim-emm-glossary.md)
- [How Citrix made apps Worx-enabled with MDX wrapping](mdx-worx-app-wrapping.md)
- [MDX and the MDX Vault: containerizing corporate mobile apps](mdx-mobile-app-containerization.md)
- [IGEL UD Pocket: a USB stick that turns any PC into a thin client](igel-ud-pocket-usb-thin-client.md)

## Security
- [Fewer components in the DMZ is more secure (durable principle)](fewer-components-in-dmz-is-more-secure.md)
- [A framework for deciding DMZ vs internal LAN server placement](dmz-placement-decision-framework.md)
- [CVE-2019-19781 Citrix ADC / SD-WAN vulnerability (2020 context)](cve-2019-19781-citrix-adc.md)
- [Securing StoreFront connections with SSL](securing-storefront-connections-with-ssl.md)

## Windows servicing, Office and licensing
- [Windows 10 servicing branches and deployment rings](windows10-servicing-branches-rings.md)
- [Microsoft VDA vs RDS licensing for Citrix](microsoft-vda-rds-licensing-for-citrix.md)
- [Microsoft RDS CALs and the XenApp vs XenDesktop split](microsoft-rds-cals-with-xenapp.md)
- [OS Migration Is More Than Swapping the OS](os-migration-is-more-than-the-os.md)
- [O365 ProPlus deployment and update channels](o365-update-channels-model.md)
- [Office 365 ProPlus on RDS: Shared Computer Activation](office-365-proplus-on-rds-shared-computer-activation.md)

## Posities
- [BYOD has graduated from hype to something you can't ignore](byod-from-hype-to-unavoidable.md)
- [Prefer PowerShell over the GUI for Citrix FMA work](powershell-over-gui-for-citrix.md)
- [The community's success depends on us; give before you take](stance-give-to-the-community.md)
- [Use one UEM layer across physical, virtual, on-prem and cloud](one-uem-layer-across-physical-virtual-cloud.md)
- [Use health-check tooling proactively, not only when things fall apart](use-monitoring-proactively-not-when-it-breaks.md)
- [Listen to the employee, don't let IT dictate how they work](listen-to-the-employee-not-it-dictates.md)
- [Technology Should Never Be Leading](technology-should-never-be-leading.md)
- [Non-persistent plus layering = the best of both worlds](non-persistent-feels-persistent-with-layering.md)
- [App layering that keeps the base image clean is the right model for AVD](positie-app-layering-keeps-the-image-clean.md)
- [Printing is the perennial pain admins shouldn't have to focus on](printing-is-a-perennial-euc-pain.md)
- [Don't be fooled: DaaS marketing sells a client desktop you aren't actually getting](daas-marketing-vs-reality.md)
- [Split tunneling's convenience carries a real, not far-fetched, security risk](positie-split-tunneling-security-tradeoff.md)
- [App attach is rebranded layering, but Microsoft's marketing will make it win](msix-app-attach-marketing-will-make-it-popular.md)
- [Measure to know (meten = weten)](measure-to-know-meten-is-weten.md)
- [WFH is not going away anytime soon](wfh-is-here-to-stay-2020.md)
- [Citrix's problem is integration and focus, not lack of products](positie-citrix-should-integrate-not-just-build.md)
- [Liquidware is a US success but underrated in Europe](liquidware-underrated-in-europe.md)
- [Workspace/app lifecycle management is an unfairly neglected discipline](lifecycle-management-neglected-unfairly.md)
- [LTSR is the right call, but not for everybody](ltsr-is-not-for-everybody.md)
- [Citrix Cloud is almost always pricier than on-prem](position-citrix-cloud-is-almost-always-pricier-than-on-prem.md)
