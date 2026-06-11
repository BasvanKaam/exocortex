---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-10
tags: [linux-vda, centos, openjdk, postgresql, ctxsetup, winbind]
layer: reference
gedateerd: ja
bron: basvankaam-blog
---

# Linux VDA install dependencies and ctxsetup.sh configuration

How it worked then (2015, guest content by Mick Glover): installing the Citrix Linux VDA v1.0 (XA/XD 7.6 FP2) on CentOS 6.6 required OpenJDK 1.7.0 and a local PostgreSQL (postgresql-server, postgresql-devel, postgresql-jdbc; initdb, chkconfig on, service start). The VDA RPM was copied over via a Windows share (using xRDP into the GUI) and installed, pulling dependent RPMs. Configuration was driven by the /usr/local/sbin/ctxsetup.sh script, where you supplied the DDC FQDN, chose to register the service on boot, add firewall exceptions, pick AD integration method (e.g. Winbind), username format, and start the XDL service. The RTW VDA (XenDesktopVDA-1.0.0.161-0) added options like allowing DDC names via CNAMEs and choosing the registration TCP port (default 80). Two services should end up present and running: ctxhdx and ctxvda. This is dated v1.0 detail, kept as a record of the Linux VDA's first shape.

*Bron: blogpost '@XDtipster - Linux VDA setup on CentOS 6.6 Pt.2' (2015-07-22), basvankaam.com.*

## Verwante notities

- [A Citrix external logon validates against LDAP three times](citrix-three-ldap-validations-logon.md)
- [The FMA core services and how they communicate](fma-services-complete-overview.md)
- [Using CentOS 6.6 to test the Citrix Linux VDA (unsupported but code-close to RHEL)](linux-vda-centos-unsupported-but-usable-for-testing.md)
- [Delivering Linux shared hosted desktops: controller, catalog and delivery group setup](linux-vda-controller-and-catalog-config.md)
- [Inspecting prerequisites up front saves the whole deployment](prerequisites-discipline-saves-time.md)
- [The VDA: client-side component, services and registration](vda-overview-services-and-registration.md)
- [VDA registration: auto-update, fallback locations and the CBP](vda-registration-process.md)
- [XenApp/XenDesktop 7.12 new features and the CR/LTSR model](xenapp-712-whats-new.md)
