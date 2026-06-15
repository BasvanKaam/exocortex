---
type: index
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-15
tags: [index, navigatie, nerdio]
---

# nerdio - index

Map of content for the Nerdio domain: Bas's Field CTO work on Azure Virtual Desktop and Windows 365, the Nerdio product line (NMW/NME/NMM), and the community, enablement and L&D practice around it. Hub notes lead each section.

## Autoscaling & cost optimization
- [Nerdio autoscaling engine: pooled hostpool scaling logic](nerdio-autoscaling-engine-pooled-hostpools.md)
- [Nerdio Cost-Optimization Levers (Bas's Assessment Method)](nerdio-cost-optimization-levers.md)
- [How Nerdio's WVD autoscale worked: triggers, base/burst capacity, graceful drain](nerdio-autoscale-mechanics-2020.md)
- [What the Nerdio autoscale engine does (NMW era)](nmw-autoscale-engine-capabilities.md)
- [Nerdio Manager for WVD: the cost-saving levers (WVD era)](nmw-cost-saving-levers-overview.md)
- [Static vs dynamic host pools in Nerdio (autoscale eligibility)](nerdio-static-vs-dynamic-host-pools.md)
- [Nerdio autoscaling for personal/persistent desktops](nerdio-autoscaling-personal-persistent-desktops.md)
- [AVD Cost Modelling: Modeler + User Cost Attribution](avd-cost-modelling-modeler-and-cost-attribution.md)
- [AVD cost-component breakdown](avd-cost-component-breakdown.md)
- [Five (plus RI) AVD cost-reduction options](avd-five-cost-reduction-options.md)
- [Settings for Success: Nerdio cost-optimization checklist](nerdio-settings-for-success-cost-checklist.md)
- [Framing a native-vs-Nerdio WVD business case](native-vs-nerdio-wvd-business-case-framework.md)

## Reserved instances, Azure pricing & licensing
- [Azure Reserved Instances: How They Work and When to Use Them](azure-reserved-instances-explainer.md)
- [Reserved Instances Do Not Guarantee Compute Availability](reserved-instances-do-not-guarantee-compute.md)
- [Azure Hybrid Benefit and the Linux-Pricing 'Fun Fact'](azure-hybrid-benefit-explainer.md)
- [Estimating WVD cost for under-100-user environments with the Azure calculator](wvd-azure-calculator-small-environment-method.md)
- [Azure GPU VMs: NVIDIA vs AMD NVv4, licensing and partitioning](azure-gpu-vms-licensing-and-nvv4-partitioning.md)
- [Nerdio consumption-based licensing model](nerdio-licensing-model.md)

## Ephemeral OS disks
- [Ephemeral OS Disks for AVD: free, fast OS storage for stateless hosts](ephemeral-os-disks-for-avd.md)
- [How Nerdio makes Ephemeral OS Disks practical (JIT provisioning + image shrink)](nerdio-ephemeral-disks-jit-and-image-shrink.md)
- [Azure Ephemeral OS Disks (and Why They Fit Stateless AVD/WVD)](azure-ephemeral-os-disks-explainer.md)
- [Turning the Ephemeral 'No Deallocate' Constraint Into a Win With Autoscaling](ephemeral-disk-constraint-vs-autoscaling.md)

## Nerdio products & architecture (NMW / NME / NMM)
- [Nerdio Manager for WVD deploys into your own Azure tenant](nerdio-manager-wvd-deploys-in-your-tenant.md)
- [Nerdio Manager for WVD core capabilities circa 2020](nmw-core-capabilities-2020.md)
- [NMW architecture: PaaS-only deploy, metering-only billing](nmw-paas-architecture-and-billing-model.md)
- [Installing Nerdio Manager for WVD from the Azure Marketplace](nmw-install-from-azure-marketplace.md)
- [Permissions to Install and Operate Nerdio (NME)](nerdio-install-and-linking-permissions.md)
- [NMM architecture: native Azure PaaS deployed into the MSP's own tenant](nmm-architecture-paas-in-msp-tenant.md)
- [Why Nerdio built a multi-tenant MSP product on top of split-tenant NMW](nerdio-manager-for-msp-why-multi-tenant.md)
- [NMW Community Edition: what it is and how to run it on a budget](nmw-community-edition-explainer.md)
- [NME / AVD troubleshooting cheat sheet](nme-troubleshooting-cheatsheet.md)
- [Azure API limits and Nerdio's API Limit Booster](nerdio-azure-api-limit-booster.md)

## AVD / WVD platform & deployment
- [Onboarding an existing WVD deployment into Nerdio (non-disruptive)](onboarding-existing-wvd-into-nerdio-non-disruptive.md)
- [WVD prerequisites Nerdio still relies on: AD sync and FSLogix profiles](nerdio-wvd-prerequisites-ad-fslogix.md)
- [NMW Deployment: What to Have Ready Before You Install](nmw-deployment-prereqs-checklist.md)
- [Size virtual desktops by testing, not by general guidelines](wvd-sizing-test-dont-trust-guidelines.md)
- [Running AVD On-Premises via Azure Stack HCI](avd-on-premises-via-azure-stack-hci.md)
- [AVD / NME outbound firewall allow-list](avd-nme-outbound-firewall-allowlist.md)
- [AVD/Azure project readiness framework](avd-project-readiness-framework.md)

## Image management
- [Nerdio image lifecycle: import, update, re-image](nerdio-image-lifecycle-import-update-reimage.md)
- [NME image management: prefer the compute gallery over the source VM](nme-image-management-gallery-vs-source-vm.md)
- [AVD/WVD Image Management Capabilities with Nerdio](avd-image-management-with-nerdio.md)
- [Automating the Patch Tuesday image lifecycle in Nerdio](nerdio-patch-tuesday-image-lifecycle-method.md)
- [Scoping desktop images: what to avoid on an image source VM](nerdio-image-source-vm-scoping-pitfalls.md)
- [Staging desktop images and auto-activation](nerdio-image-staging-auto-activation.md)

## Application management, MSIX App Attach & layering
- [A six-pillar application management strategy for AVD](avd-application-management-strategy-six-pillars.md)
- [Setting up MSIX App Attach v2 in Nerdio and publishing apps](msix-appattach-v2-publish-nerdio.md)
- [Unified Application Management: four key concepts](nerdio-uam-four-key-concepts.md)
- [Application layering toward a zero-app golden image](application-layering-zero-apps-in-golden-image.md)

## Storage & FSLogix
- [Nerdio Manager storage autoscale for Azure Files Premium](nerdio-azure-files-premium-autoscale.md)
- [Azure Files tiers and pricing model (reference)](azure-files-tiers-reference.md)

## Disaster recovery & high availability
- [DR/HA Discovery Questions for AVD and Nerdio](dr-ha-discovery-questions-avd.md)
- [Active/Active DR for AVD Across Two Regions](nerdio-active-active-dr.md)
- [AVD High Availability: Availability Sets vs Zones and Redundant Storage](avd-high-availability-sets-zones-storage.md)
- [Nerdio AVD resilience and DR features](nerdio-avd-resilience-features.md)
- [Disaster recovery for WVD: keep machines off until needed](wvd-disaster-recovery-cost-angle.md)

## Security & hardening
- [Hardening the Nerdio Manager Console Itself](nerdio-manager-hardening-checklist.md)
- [Hardening Nerdio and AVD: Easy Way vs Hard Way](hardening-nerdio-avd-easy-vs-hard.md)
- [AVD Security Checklist by Layer (Bas's Cheat Sheet)](avd-security-checklist-by-layer.md)
- [AVD Security cheat sheet v2.0 — 44 best practices](avd-security-cheat-sheet-v2.md)
- [AVD Shared Responsibility: Who Secures What](avd-shared-responsibility-model.md)
- [Hardening Nerdio Manager for MSP: the private-endpoint pattern](nmm-hardening-private-endpoint-pattern.md)
- [Hardening NME with private endpoints (the full approach)](nme-hardening-private-endpoints.md)
- [Delegated vs Application Permissions (Microsoft Graph)](delegated-vs-application-permissions-graph.md)

## Zero Trust
- [Zero Trust principles mapped to AVD and Windows 365 in NME](zero-trust-mapped-to-avd-w365-nme.md)
- [Zero Trust Identity Controls in Nerdio (AVD + W365)](zero-trust-controls-nerdio-avd-w365.md)
- [Zero Trust extras: patching cadence and CIS-hardened images](zero-trust-hardening-extras-patch-cis-images.md)
- [Mapping Zero Trust Principles to Real NME Capabilities](mapping-zero-trust-to-nme-capabilities.md)

## Windows 365 / Cloud PC
- [Cloud PC vs AVD: a four-lens decision framework](cloud-pc-vs-avd-decision-framework.md)
- [Windows 365 Cloud PC: What It Is and How It Differs from AVD](w365-cloud-pc-vs-avd-fundamentals.md)
- [Where Nerdio adds value on top of native Cloud PC](nerdio-added-value-on-cloud-pc.md)
- [Cloud PC licensing requirements (durable)](cloud-pc-licensing-requirements.md)
- [Why Windows 365 enablement needs Global Admin (org consent)](windows-365-enablement-permissions.md)
- [Windows 365 License Optimization: The Three Levers](w365-license-optimization-method.md)
- [Windows 365 Reserve (Cloud PC panic button)](windows-365-reserve-explainer.md)
- [Windows 365 Frontline: concurrency licensing for shift/frontline workers](windows-365-frontline-concurrency-model.md)

## Scripted Actions & automation
- [What Nerdio Scripted Actions are](nmw-scripted-actions-explainer.md)
- [Nerdio Scripted Actions: scripting criteria & predefined variables](nerdio-scripted-actions-scripting-criteria.md)
- [NME hybrid worker vs inline-script runbook execution](nme-hybrid-worker-and-inline-runbooks.md)
- [Patch Tuesday: fully automated image patching in Nerdio](nerdio-patch-tuesday-image-automation.md)
- [Nerdio self-service portal: delegated machine control for power users](nerdio-self-service-portal-user-control.md)

## Migration (WVD Classic → ARM, NME → NMM)
- [NME to NMM migration runbook (AVD)](nme-to-nmm-migration-runbook.md)
- [WVD Classic to ARM migration: the two-step pattern](wvd-classic-to-arm-two-step-migration.md)
- [Migrating WVD from Tenant to Workspace (ARM) in Nerdio](wvd-tenant-to-workspace-arm-migration.md)
- [Moving images and AVD objects from NME to NMM via Azure tags](nerdio-nme-to-nmm-image-migration-via-tags.md)
- [Hybrid WVD Object Model (NMW, Fall/Spring era)](nmw-hybrid-wvd-object-model.md)

## Sales, discovery & business case
- [AVD / Windows 365 Discovery Questions (Bas's Talking Points)](avd-w365-discovery-questions.md)
- [Bas's Nerdio pitch structure: the value-add narrative arc](nerdio-five-pillar-pitch-structure.md)
- [Method: Agree PoC Success Criteria Up Front](method-poc-success-criteria.md)
- [Vertical-tailored discovery deck for smaller opportunities](vertical-discovery-deck-method.md)
- [Idea: Your Nerdio configuration as your best sales tool](idee-nerdio-config-as-sales-tool.md)

## MSP practice
- [Idea: Turn recurring MSP work into repeatable revenue with Nerdio](idee-nerdio-recurring-work-repeatable-revenue.md)
- [Idea: Nerdio vs shadow IT](idee-nerdio-shadow-it-governance.md)
- [Idea: The self-healing MSP environment](idee-self-healing-msp-environment.md)
- [NMM's four customer onboarding scenarios and what each reuses](nmm-customer-deployment-scenarios.md)

## Community & NVP program
- [Build a practitioner community as a go-to-market motion](community-program-as-go-to-market-idea.md)
- [NVP Captains: Seeding a Community Program With Founding Members](nvp-captains-model.md)
- [Designing a Community Advocate Program (NVP)](nvp-community-advocate-program-design.md)
- [NVP Program: How Bas Onboards Community Members](nvp-program-onboarding-playbook.md)
- [NVP Newsletter: Bas's Recurring Community Update Format](nvp-newsletter-format.md)
- [Idea: crowdsource the Scripted Actions library from the community](idea-community-scripted-actions-library.md)
- [The content and channel stack behind a community launch](community-launch-content-engine.md)

## Events & enablement
- [The Innovation Day / MicroHack hands-on event format](nerdio-innovation-day-microhack-format.md)
- [Two event types: Training Camp vs Innovation Day](etc-vs-innovation-day-event-design.md)
- [Nerdio's four lab-driven event formats](nerdio-lab-driven-event-formats.md)
- [Idea: Nerdio Fusion - a merged event format](idee-nerdio-fusion-merged-event-format.md)
- [How Bas designs a self-paced MicroHack lab](microhack-lab-design-method.md)
- [XpressLabs: Bas's Innovation-Day-in-a-box teaching method](xpresslabs-innovation-day-in-a-box-method.md)
- [Nerdio Scripted Actions Hackathon: Bas's Community Event Format](nerdio-scripted-actions-hackathon-concept.md)

## L&D & training method
- [The Nerdio training creation framework (Bas's L&D method)](nerdio-training-creation-framework.md)
- [Training Method: Bringing Field Experience Into the Classroom](trainer-method-field-experience-to-classroom.md)
- [Method: The Learning Pyramid Applied to Technical Training](learning-pyramid-training-method.md)
- [Bas's ADDIE course-planning method](addie-course-planning-method.md)
- [Method: Bas's Nerdio lab-guide template convention](method-nerdio-lab-guide-template.md)
- [How Bas reviews Nerdio L&D content as SME](nme-course-content-review-method.md)
- [The Nerdio Enterprise Optimization Journey (12-step framework)](nerdio-enterprise-optimization-journey.md)
- [Nerdio Adoption & Management Framework: Five Foundational Elements](nerdio-adoption-management-framework.md)

## Career & Field CTO role
- [Bas joined Nerdio as Field CTO EMEA on 1 June 2020](bas-joins-nerdio-field-cto-emea.md)
- [What the EMEA Field CTO role covers (Bas's own description)](bvk-nerdio-field-cto-role.md)
- [Bas's Field CTO mandate at Nerdio (the brief he set himself)](field-cto-role-mandate.md)
- [Nerdio Manager for WVD launched March 2020 with fast traction](nerdio-manager-wvd-early-traction.md)
- [Nerdio Manager for WVD roadmap as of mid-2020](nerdio-2020-product-roadmap-snapshot.md)

## Posities (Bas's stances)
- [The NMW thesis: automation and hiding complexity](nmw-thesis-automation-hiding-complexity.md)
- [Microsoft's WVD power scripts are not real autoscaling](nerdio-vs-microsoft-power-management-scripts.md)
- [Bet: WVD third-party vendors are where the action is](betting-on-wvd-third-party-tooling-2020.md)
- [Community feedback as the force that shapes the product](community-as-product-shaping-force.md)
- [Be a Learn-It-All Organization, Not a Know-It-All One](learn-it-all-not-know-it-all.md)
- [The real win of WVD automation is reclaimed admin time, not just compute](automation-saves-time-equals-money-position.md)
- [Nerdio's real payoff is reclaimed engineer time, not just Azure cost](value-is-time-reclaimed-not-just-cost.md)
- [The True ROI Is Time and Wellbeing, Not Just Money](position-true-nerdio-roi-is-time-and-wellbeing.md)
- [Good UI is a business strategy, not decoration](positie-ui-as-product-strategy.md)
- [Lead with operational and business value; cost savings is the cherry on top](lead-with-operational-value-not-just-cost.md)
- [Autoscaling can beat Reserved Instances, and pairs with them](autoscaling-vs-reserved-instances.md)
- [Auto-scale first, then reserve the residual](auto-scale-before-reserved-instances.md)
- [For steady WVD workloads, reserved instances almost always win](reserved-instances-almost-always-cheaper-position.md)
- [Microsoft builds the core, Nerdio closes the management feature gap](microsoft-builds-the-plane-nerdio-fills-the-gap.md)
- [Nerdio innovating on top of WVD is 'a perfect marriage'](nerdio-plus-microsoft-perfect-marriage.md)
- [WVD with Nerdio on top is the new 'RDS with Citrix on top'](wvd-with-nerdio-on-top-citrix-framing.md)
- [Microsoft has won the VDI war; AVD is the DaaS leader](microsoft-has-won-the-vdi-war.md)
- [Security is always a fine line against user experience](avd-security-vs-user-experience-balance.md)
- [Nerdio Is Not Secure Out of the Box, So Always Harden](positie-nerdio-not-secure-out-of-the-box.md)
- [Nerdio Manager Is an Orchestration Layer, Not a Security Product](position-nerdio-is-orchestration-not-a-security-product.md)
- [DR Is About Apps and Data, Not Fancy Infrastructure](positie-dr-is-about-apps-and-data.md)
- [Don't Spend Budget Making the AVD Management Tool Highly Available](dont-make-the-avd-management-plane-highly-available.md)
- [Simplicity comes at the cost of flexibility](simplicity-costs-flexibility.md)
- [Windows 365 and AVD Are Complementary, Not Competing](positie-w365-and-avd-coexist.md)
- [AVD and Cloud PC go hand in hand, pick per use case](positie-avd-en-cloud-pc-gaan-hand-in-hand.md)
- [Ephemeral OS Disks are underrated for stateless AVD](positie-ephemeral-os-disks-underrated.md)
- [Call them traditional Windows apps, not legacy, and AVD keeps them alive](position-traditional-not-legacy-windows-apps.md)
- [MSPs should charge per outcome, not per hour](positie-charge-per-outcome-not-per-hour.md)
- [Building an MSP cloud practice rests on three pillars](msp-cloud-practice-three-pillars.md)
- [Show, don't sell](positie-show-dont-sell.md)
- [Lead enablement with hands-on labs, not slideware](hands-on-labs-over-slideware.md)
- [Active Learning Beats Passive: Design Training for Retention, Not Coverage](position-active-learning-beats-passive.md)
- [Training content must be technically true and honestly named](training-must-be-technically-true.md)
- [Generic security awareness fails; training must be role-based](position-security-awareness-must-be-role-based.md)
- [Teaching Philosophy: Simplify, Educate, Empower](teaching-philosophy-simplify-and-empower.md)
- [Everyone sweeps the floor (the Nerdio culture stance)](position-everyone-sweeps-the-floor.md)
- [Concentrated cloud knowledge in a few seniors is a business risk](knowledge-leaving-the-company-as-a-real-risk.md)
- [The two kinds of sysadmin, and why 80% of IT should not have to go all-in](two-kinds-of-sysadmin-and-the-80-percent.md)
- [Real multi-tenancy keeps the MSP in control of its own tenant, not a shared plane](true-multi-tenancy-vs-shared-management-plane.md)
- [Don't hide costs from customers: full-disclosure pricing builds trust](radical-pricing-transparency-position.md)
- [Moving VDI to the cloud shifts emissions from Scope 2 to Scope 3](vdi-to-cloud-emissions-scope-shift.md)
