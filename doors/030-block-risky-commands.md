# Door 30: Block risky commands before an AI runs them: safety checks for Claude Code, with limits

- **Date:** November 13, 2026
- **Built:** June 20, 2026
- **Room:** Checks (6 of 7)
- **Gift:** [harness-guard](https://github.com/LucasCooperBey/harness-guard)

## What it is

An AI coding agent can damage files too. harness-guard is eight Claude Code hooks that refuse risky agent turns, including destructive commands, force pushes to main, secrets leaving the machine, and edits that weaken your linter. It builds on Door 12, which shared four of them.

These hooks are a seatbelt for accidents and for the most common bad turns, not a sandbox. They reduce some risks, not all of them.

## Try it today

**The gift:**

[https://github.com/LucasCooperBey/harness-guard](https://github.com/LucasCooperBey/harness-guard)

Clone the repo, run ./install.sh, merge the hooks block from settings.example.json into ~/.claude/settings.json, and restart Claude Code.
100 Doors to Recursion https://github.com/LucasCooperBey/100-doors
