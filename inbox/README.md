---
type: index
merk: bvk
domein: persoonlijk
status: actief
datum: 2026-10-02
tags: [inbox, notes-on-the-go, workflow]
---

# Inbox

Raw notes land here first. Most of them are dictated on my phone, so expect rough edges. Nothing in this folder is final.

## How notes get here

- A message that starts with "Note:" or "Notitie:" becomes a new file in this folder.
- File name: `YYYY-MM-DD-short-title.md`.
- Always stored in English, even when dictated in Dutch. Proper names and Dutch project names stay as they are.
- Lightly cleaned up (punctuation, spelling, terms like Nerdio, AVD, Windows 365, Intune, Docebo). The content itself is not changed.
- Frontmatter carries the date and `source: phone`.

## What happens next

When I say "process the inbox" (or "verwerk de inbox"), Claude proposes a destination for each note: a new file in `kennis/`, `beslissingen/` or `standaarden/`, or an addition to an existing note. Nothing moves until I approve. After that: move, link, commit, push.

The full rules live in `CLAUDE.md` under "Notes on the go" and "Processing the inbox". Maintenance rules: `standaarden/brein-onderhoud.md`.

## Related notes

- [Hoe we het brein vullen: de intake-pijplijn](../beslissingen/brein-intake-pijplijn.md)
