# Door 49: I ask real models before I make the call: a Claude Code skill where each seat writes first, its model is read from the harness record, and dissent is kept by name

- **Date:** November 26, 2026
- **Built:** November 16, 2026
- **Room:** 5
- **Gift:** [council](https://github.com/LucasCooperBey/claude-skills/tree/main/skills/council)

## What it is

I ask real models before I make the call. One model is a single view on an open choice. Each seat writes its position before seeing another seat, and the seats cross-examine one another under neutral labels. The model id is read from the harness record, because a model naming itself is not proof.

council is a Claude Code skill. It needs Claude Code signed in on a plan, and jq to read each seat's model id. It ships with a three-seat roster of opus, sonnet and haiku through claude -p, a written method and one real run's full result. Agreement among models is not market evidence.

On the three-seat roster it ships with, every model holds a seat, so the final check reuses a seat's model and the result says the review is not independent.

## Try it today

**The gift:**

[https://github.com/LucasCooperBey/claude-skills/tree/main/skills/council](https://github.com/LucasCooperBey/claude-skills/tree/main/skills/council)

Clone LucasCooperBey/claude-skills, run mkdir -p ~/.claude/skills, copy skills/council into ~/.claude/skills, then ask Claude Code to run a council on an important, uncertain choice. It needs Claude Code signed in on a plan, and jq.
100 Doors to Recursion https://github.com/LucasCooperBey/100-doors
