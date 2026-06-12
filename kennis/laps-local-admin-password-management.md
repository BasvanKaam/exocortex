---
type: kennis
merk: bvk
domein: cloud
status: actief
datum: 2026-06-11
tags: [laps, security, active-directory, server-hardening, local-admin, microsoft]
layer: reference
gedateerd: ja
bron: cgit-blog
---

# LAPS for managing local admin passwords

The problem: every server has a local administrator account with very high privileges (it is how you get back in when a server is pulled from the domain), yet it is the account nobody looks after — often with no unique password. When servers are rolled out from a template or an automated method, they tend to share one password. If an attacker finds one server's password, they have all of them, including servers holding important company documents.

The solution: give every server its own complex, unique, regularly rotated password. Done by hand this is administration no admin wants, and periodic rotation even less so — which is why password managers so often hold a single shared local-admin password.

Microsoft's Local Administrator Password Solution (LAPS) automates this:
- It is an extension of Active Directory, so it requires no extra server or server role; servers do need the LAPS Group Policy Extension installed.
- A Group Policy sets rotation frequency and password requirements; LAPS then automatically rotates each local admin password to a unique generated value and stores it in Active Directory.
- Passwords are managed centrally via a Group Policy Object.

Watch out for: restoring a VM backup, which likely holds an older local-admin password. If that older password was not written down anywhere, it cannot be recovered. LAPS can be made to store passwords automatically in a separate place for this scenario, but that requires a custom script.

Takeaway: LAPS shows that parts of server hardening can be genuinely easy — there is no longer any excuse to leave local-admin password management unmanaged. (Related: server hardening, covered by colleague Sander Bruijs.)

*Bron: Salomon-IT 'SBC - LAPS technisch V2 - BvK' (CGIT Blogs).*

## Verwante notities

- [Challenges of getting and staying PCI DSS and PTS certified](pci-dss-pts-certification-challenges.md)
- [Policy is the starting point of every IT project](policy-as-the-start-of-every-it-project.md)
- [Security is a process, not a destination](security-is-a-process-not-a-destination.md)
- [Server hardening can be easy — so there is no excuse](server-hardening-can-be-easy-no-excuse.md)
