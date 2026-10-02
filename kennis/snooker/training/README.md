---
type: index
merk: bvk
domein: snooker
status: actief
datum: 2026-10-02
tags: [snooker, training, trainingslog, index]
---

# Snooker training log

Short log of my snooker practice sessions. Goal: be able to answer over time which week or month I practiced most, and what I focused on.

## Convention
- One file per session: `JJJJ-MM-DD-training.md` (second session on the same day: `JJJJ-MM-DD-training-2.md`).
- Entries come in by voice, Dutch or English, and are stored in English. Light cleanup only, no additions.
- Frontmatter fields `duration_min` and `focus` are the basis for analysis per week or month. `focus` uses short, consistent terms in lowercase (for example: `long-potting`, `break-building`, `safety`, `cue-action`, `positional-play`, `cushion-shots`, `rest-play`, `line-up`). Reuse existing terms before inventing new ones.
- Unknown values (for example no duration mentioned) are left out, never guessed.

## Template

```markdown
---
type: bron
merk: bvk
domein: snooker
status: actief
datum: JJJJ-MM-DD
source: phone
duration_min: 90
focus: [long-potting, safety]
tags: [snooker, training]
---

# Training JJJJ-MM-DD

## Focus
What I worked on.

## Drills
- Drill, with result or score if mentioned.

## Notes
Observations, what went well, what to work on next.

Back to: [Snooker training log](README.md)
```

## Sessions
Newest at the top.

## Related
- [snooker - index](../../index-snooker.md)
