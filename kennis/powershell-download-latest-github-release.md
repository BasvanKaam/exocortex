---
type: kennis
merk: bvk
domein: euc
status: actief
datum: 2026-06-11
tags: [powershell, github-api, automation, snippet, remote-display-analyzer]
layer: reference
gedateerd: nee
bron: nerdio-content
---

# PowerShell: download the latest release asset from GitHub

Reusable pattern for pulling the latest (or a named) release binary straight from a GitHub repo without hardcoding a URL. Useful for keeping EUC tools like Remote Display Analyzer current in scripts and lab automation.

Approach:
- Hit `https://api.github.com/repos/<Repository>/releases` with `Invoke-RestMethod`.
- For latest, take element `[0]` of the returned array (the API returns releases newest-first). For a specific version, filter `Name -like "*<Version>*"` and throw if zero or multiple match.
- From the chosen release's `assets`, select the wanted asset by name pattern (here `*RemoteDisplayAnalyzer.exe`), read `browser_download_url`, and download with `Invoke-WebRequest`.
- Create the download path if missing; wrap each external call in try/catch and throw a descriptive error including the URI and `$_.Exception.Message`.
- Return a `[PSCustomObject]` with `Version` and `Download` path.

Example call: `Get-GitHubRelease -Repository "RDAnalyzer/release" -DownloadPath "C:\Temp"`.

Reusable details worth remembering: the GitHub releases API needs no auth for public repos, releases come back newest-first, and asset selection should be pattern-based so it survives version bumps in the filename.

*Bron: Nerdio-content 'Get-GitHubLatestRDARelease' (Community Tech Insider).*

## Verwante notities

- [Idea: crowdsource the Scripted Actions library from the community](idea-community-scripted-actions-library.md)
- [Nerdio Scripted Actions: scripting criteria & predefined variables](nerdio-scripted-actions-scripting-criteria.md)
- [What Nerdio Scripted Actions are](nmw-scripted-actions-explainer.md)
- [Using PowerShell to check FMA service states](powershell-fma-service-checks.md)
- [Remote Display Analyzer: a community HDX codec tool](remote-display-analyzer.md)
- [Remote Display Analyzer: detect and live-switch HDX codecs](remote-display-analyzer-tool.md)
