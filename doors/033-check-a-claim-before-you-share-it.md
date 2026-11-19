# Door 33: I check a claim before I share it: separate what the sources support from what they don't

- **Date:** November 19, 2026
- **Built:** June 20, 2026
- **Room:** 4
- **Gift:** [adversarial-research](https://github.com/LucasCooperBey/claude-skills/tree/main/skills/adversarial-research)

## What it is

A confident answer can still rest on a source that says something else. adversarial-research sends separate verifier agents after each claim and sorts what the sources support from what they don't. A run costs about 200 agents and 20 minutes. The idea came from Mark Kashef's Dynamic Workflows prompt pack; the skill's Source section says so.

It needs agent research tools and independent verifier agents. A supported claim is only as good as the sources it found.

## Try it today

**The gift:**

[https://github.com/LucasCooperBey/claude-skills/tree/main/skills/adversarial-research](https://github.com/LucasCooperBey/claude-skills/tree/main/skills/adversarial-research)

Clone LucasCooperBey/claude-skills, copy skills/adversarial-research into ~/.claude/skills, then in Claude Code ask it to use the skill on a draft and extract the claims first. The verifier pass waits for you to opt in.
100 Doors to Recursion https://github.com/LucasCooperBey/100-doors
