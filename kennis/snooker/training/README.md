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
- Entries come in by voice, Dutch or English, and are stored in English. Light cleanup only, no additions. The order in which I tell it varies; the file always follows the template below.
- Every session has one primary focus and a few secondary elements in between. I do a bit of everything each session; what changes is where the weight lies.
- Frontmatter fields for analysis per week or month: `duration_min`, `focus_primary` (one term) and `focus_secondary` (list). Use short, consistent lowercase terms and reuse existing ones before inventing new ones:
  - `colours-round-the-table`: the small game, colours from their spots into all pockets with sharp and obtuse angles.
  - `long-potting`: long pots.
  - `break-building`: clearing several reds with colours.
  - `clearance`: clearing the table, positional play.
  - `safety`, `cue-action`, `cushion-shots`, `rest-play`, `line-up`: as named.
- Unknown values (for example no duration mentioned) are left out, never guessed. Leave out `focus_primary` and `focus_secondary` when no focus was given.
- Durations are always written in minutes, in frontmatter and text. "Just over" (ruim) becomes the lower bound with a plus: just over an hour = `60+`, just over an hour and a quarter = `75+`, just over an hour and a half = `90+`, just over two hours = `120+`. In frontmatter `duration_min` holds the number only (60), in text it reads "60+ minutes".
- Sessions are always logged, also afterwards and also with only a duration. The real training date goes in `datum` and in the file name.

## Template

```markdown
---
type: bron
merk: bvk
domein: snooker
status: actief
datum: JJJJ-MM-DD
source: phone
duration_min: 72
focus_primary: colours-round-the-table
focus_secondary: [long-potting, break-building, clearance]
tags: [snooker, training]
---

# Training JJJJ-MM-DD

## Summary
Two or three sentences: duration, primary focus, what came in between, overall verdict.

## Primary focus
What I worked on most, with the drills.

## In between
Secondary elements, with drills and amounts if mentioned.

## Concentration
How focus went over the session, and what disturbed it.

## Notes
Observations, what went well, what to work on next. Leave out if nothing was said.

Back to: [Snooker training log](README.md)
```

## Sessions
Newest at the top.
- [2026-10-02](2026-10-02-training.md): 72 min, primary `colours-round-the-table`
- [2026-10-01](2026-10-01-training.md): 90+ min, focus not recorded
- [2026-09-30](2026-09-30-training.md): 30+ min, focus not recorded
- [2026-09-29](2026-09-29-training.md): 90+ min, focus not recorded
- [2026-09-28](2026-09-28-training.md): 60+ min, focus not recorded

## Related
- [snooker - index](../../index-snooker.md)
- [Snooker and my career: LinkedIn newsletter series](../newsletter/README.md)
