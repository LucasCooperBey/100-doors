# The dated decision entry

When you decide something that matters, write one short file before you move on. Six months later the code will show what you did. Only this file will show why, and what you turned down.

One decision per file. Name it with the date first, so the folder sorts itself into a timeline: `2026-05-02-move-the-newsletter-to-weekly`, saved as a Markdown file.

## The template

```markdown
---
date: YYYY-MM-DD
decided_by: [who made the call]
tags: [two to six words you would search for later]
summary: >
  One to three sentences: what was decided and the main reason.
  Write it for someone who reads only this part.
confidence: high | medium | low
alternatives_considered:
  - option: The first option you weighed
    rejected_because: The real reason, in one line
  - option: The second option
    rejected_because: ...
  - option: The one you picked
    chosen: true
    chosen_because: ...
sources:
  - The notes, numbers or messages that fed the decision
replaces: [the date-name of an older entry this one overrides, or leave empty]
---

## What we decided

## What would make us change it
```

## One filled in (made up)

```markdown
---
date: 2026-05-02
decided_by: [the editor]
tags: [newsletter, cadence, workload]
summary: >
  The newsletter moves from daily to weekly. Daily issues took about
  two hours each and opens fell every week after the first month.
confidence: medium
alternatives_considered:
  - option: Keep it daily
    rejected_because: Two hours a day, and opens kept falling
  - option: Stop the newsletter
    rejected_because: Replies from readers are still the best source of ideas
  - option: Weekly
    chosen: true
    chosen_because: One issue a week leaves time to make each one worth opening
sources:
  - The open rates for the last eight weeks
  - The time log for the last month
replaces: []
---

## What we decided
Weekly, starting with the next issue.

## What would make us change it
Opens falling below the daily average for a month, or readers asking for daily again.
```

## Three rules that keep it useful

1. **Never edit an old entry to change the decision.** Write a new one that names the old one in `replaces`. The old one stays, so you can still see what you believed then.
2. **Always write down what you turned down.** The rejected options are the part you will most want later, and the part nobody remembers.
3. **Keep the summary short.** If you can only read one field across a hundred entries, it is this one.

## Try it

Pick one decision you made this month. Write its entry in ten minutes, turned-down options included. Put it in a folder called `decisions/`. Next time someone asks "why did we do it this way?", send them the file.
