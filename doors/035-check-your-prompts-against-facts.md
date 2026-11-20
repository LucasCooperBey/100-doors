# Door 35: I check my prompts against facts: match a prompt's claims to your real files, then rewrite it

- **Date:** November 19, 2026
- **Built:** June 20, 2026
- **Room:** 4
- **Gift:** [prompt-grounding](https://github.com/LucasCooperBey/claude-skills/tree/main/skills/prompt-grounding)

## What it is

A prompt can describe files, names or features that aren't really there, and the agent believes it. prompt-grounding reads your docs, code and archived decisions, sorts each claim in the prompt as accurate, invented, conflated or misframed with the file and line that shows it, and rewrites the prompt to match.

It needs access to the project files being checked. It produces an audit and a revised prompt, not proof that every claim is true.

## Try it today

**The gift:**

[https://github.com/LucasCooperBey/claude-skills/tree/main/skills/prompt-grounding](https://github.com/LucasCooperBey/claude-skills/tree/main/skills/prompt-grounding)

Clone LucasCooperBey/claude-skills, copy skills/prompt-grounding into ~/.claude/skills, save the prompt you want checked as prompt.txt in your project, and ask Claude Code to use the skill on it.
100 Doors to Recursion https://github.com/LucasCooperBey/100-doors
