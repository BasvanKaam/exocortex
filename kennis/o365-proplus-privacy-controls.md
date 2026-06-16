---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [office-365, privacy, diagnostic-data, group-policy, whitepaper]
layer: reference
gedateerd: nee
bron: salomon-whitepaper
---

# Controlling ProPlus diagnostic data and connected services

From the whitepaper. ProPlus collects diagnostic data about Office client usage on user devices and sends it to Microsoft, used to keep ProPlus secure and up to date, improve the product and diagnose problems. ProPlus also offers online/connected services tied to Word, Excel, PowerPoint, Outlook (co-authoring, slide design suggestions, communication) that also gather and share information.

Microsoft provides options to limit these services and data collection so sensitive information is not sent and unnecessary data is not downloaded or analyzed without consent. Admins apply restrictions via Group Policy and/or the Office Cloud Policy Service. Some services Microsoft deems essential cannot be restricted, which warrants investigation or advice.

The principle (audit connected services, restrict via policy, mind the essential-services exception) is durable; specific service names are 2019-era.

*Bron: Salomon-IT 'Whitepaper'.*

## Verwante notities

- [ProPlus deployment and update tooling options](o365-proplus-deployment-and-update-options.md)
- [Office 365 ProPlus versus traditional Office](o365-proplus-vs-traditional-office.md)
- [ProPlus diagnostic data and privacy controls](office-365-proplus-privacy-controls.md)
- [Organizations want control over updates, not full automation](position-control-updates-dont-fully-automate.md)
