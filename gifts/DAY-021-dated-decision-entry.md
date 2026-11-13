# Remember why you decided: wiki-write and the dated decision entry

When you decide something that matters, write one short file before you move on. Six months later the code will show what you did. Only this file will show why, and what you turned down.

## The tool: wiki-write

[wiki-write](https://github.com/LucasCooperBey/claude-skills/tree/main/skills/wiki-write) is a Claude Code skill with two small scripts. The skill tells the agent when a choice is worth a note: it is hard to reverse, it would surprise a reader without the context, and it came out of a real trade-off. The scripts file the note with today's date in its name, refuse a note with a missing field or a duplicate name, and rebuild one `INDEX.md` that a later reader, or a later agent, reads first to find the right note.

Install it:

```bash
git clone https://github.com/LucasCooperBey/claude-skills.git
cp -R claude-skills/skills/wiki-write ~/.claude/skills/
```

From your project folder, the agent (or you) runs `~/.claude/skills/wiki-write/scripts/write-entry.sh decision <short-name>` with the note on standard input, then `~/.claude/skills/wiki-write/scripts/build-index.sh`. The notes land in `./wiki`, or wherever `WIKI_DIR` points. It needs bash and Python 3, and no account or key. The skill's README has a complete example you can paste.

## By hand: the template

No Claude Code? The same habit works with a text editor. The skill's notes use the fields in its SCHEMA.md; this template carries the same idea with plain field names.

One decision per file. Name it with the date first, so the folder sorts itself into a timeline: `2026-05-02-move-the-newsletter-to-weekly`, saved as a Markdown file.

### The template

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

### One filled in (made up)

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

### Three rules that keep it useful

1. **Never edit an old entry to change the decision.** Write a new one that names the old one in `replaces`. The old one stays, so you can still see what you believed then.
2. **Always write down what you turned down.** The rejected options are the part you will most want later, and the part nobody remembers.
3. **Keep the summary short.** If you can only read one field across a hundred entries, it is this one.

### Try it

Pick one decision you made this month. Write its entry in ten minutes, turned-down options included. Put it in a folder called `decisions/`. Next time someone asks "why did we do it this way?", send them the file.
