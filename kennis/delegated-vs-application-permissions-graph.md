---
type: kennis
merk: bvk
domein: nerdio
status: actief
datum: 2026-06-11
tags: [entra, microsoft-graph, permissions, security, azure]
layer: reference
gedateerd: nee
bron: nerdio-content
---

# Delegated vs Application Permissions (Microsoft Graph)

Durable explainer Bas uses when security teams push back on permissions.

- **Delegated permissions** apply in the delegated-access scenario: the app acts on a signed-in user's behalf and can never access anything the user themselves could not. Example: an app granted `Files.Read.All` delegated can only read files the user can already access.
- **Application permissions** (a.k.a. app roles) apply in the app-only scenario, with no signed-in user. The app can access any data the permission covers. Example: an app granted `Files.Read.All` application can read **any** file in the tenant via Graph. Generally only an admin or the API service principal's owner can consent to application permissions.

Field observation: security teams and customers tend to be more comfortable with **delegated** permissions because they retain more control. **Read** permissions are usually fine; `write` and `write.all` permissions are where the friction shows up.

## Consent flow
User consent triggers at sign-in: credentials are checked against existing consent; if none exists for the required permissions, the user sees a consent prompt. An admin may need to consent on the user's behalf.

*Bron: Nerdio-content 'CORE DOC... Permissions' (Core Docs).*

## Verwante notities

- [Azure API limits and Nerdio's API Limit Booster](nerdio-azure-api-limit-booster.md)
- [Permissions to Install and Operate Nerdio (NME)](nerdio-install-and-linking-permissions.md)
- [NME / AVD troubleshooting cheat sheet](nme-troubleshooting-cheatsheet.md)
- [Always Test Before Revoking API Permissions](positie-test-before-revoking-api-permissions.md)
- [Instructional Method: Teaching an API by Scope Boundary, Not by Coding](teaching-an-api-scope-boundary-not-coding.md)
- [Why Windows 365 enablement needs Global Admin (org consent)](windows-365-enablement-permissions.md)
- [Zero Trust Identity Controls in Nerdio (AVD + W365)](zero-trust-controls-nerdio-avd-w365.md)
