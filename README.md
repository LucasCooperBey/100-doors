# 100 Doors to Recursion

One door a day for 100 days into the things I've made with AI, from my first app to the system I run now.

Day 1 is Tuesday, October 13, 2026. Day 100 is Wednesday, January 20, 2027.

Each door says what the thing was and when I made it. Most doors also leave you something to use that day: a tool, a template or an exercise. Everything here is extracted fresh and checked before it goes up. Client work stays private and only shows up as a story.

## The doors

| Day | Door | Built | Gift | Something to try |
|---|---|---|---|---|
| 1 | RobotTales: bedtime stories where robot siblings teach if/else, loops and variables | March 23, 2025 | [A bedtime-story prompt that teaches one coding idea](gifts/DAY-001-bedtime-story-prompt.md) | Paste it into any chat model, fill in the three brackets, and read what comes back before you read it aloud. |
| 2 | WebPerformanceToolkit: my first app in git, and its 33 hours of simulated scores | June 26, 2025 | [The first prompt template: twelve sections plus the real-data line](gifts/FIRST-PROMPT-TEMPLATE.md) | Before your next build, fill in at least sections 1, 4, 5 and 6, then paste the whole thing as your first message. |
| 3 | My CRM, started on Replit from two pasted documents | September 18, 2025 | dataguard: checks a SQL database for orphaned records and dates out of order (link goes up when it is ready) | Pick one table in a database you own and count the rows that point at a record that no longer exists. |
| 4 | FriendForm: a form friends fill out from a link | October 9, 2025 | [A blank intake form to copy into any form tool](gifts/DAY-004-blank-intake-form.md) | Take one questionnaire you send around as a document, rebuild it from these sections and cut every question you would not act on. |
| 5 | treehouse: a git worktree pool for running several coding agents side by side | July 4, 2026 | [treehouse, one bash file that needs only git: spin a worktree per agent, glance at which are dirty on one screen, and sweep only the clean, merged ones](https://github.com/LucasCooperBey/treehouse) | Run treehouse spin 3, then treehouse glance. |
| 6 | My Claude Code config, and the ramp: a 53-second first session in May, then 146 sessions from November 8 to December 11 | November 20, 2025 | [claude-config-public: the operating-rules template](https://github.com/SanDiegoAIStudio/claude-config-public) | Copy it to ~/.claude/CLAUDE.md and fill in the 5 placeholders. |
| 7 | The perfection pass: ask for two critique passes before you look | January 9, 2026 | [pp2p and pp3p, two Claude Code skills: two or three critique passes, then a polish](https://github.com/Lucface/claude-skills/tree/main/skills/pp2p) | Before you read your agent's next piece of work, ask it for two critique passes that try to break it, then a polish. |
| 8 | The changelog that becomes content | December 4, 2025 | [changelog-digest: turn a day of changelog entries into a hook, a short story and video ideas](https://github.com/SanDiegoAIStudio/changelog-digest) | Run the dry run on the sample changelog, then on your own. |
| 9 | block-destructive: a Claude Code hook that stops destructive shell commands before the agent runs them | March 8, 2026 | [The hook: refuses rm -rf on root or home, force-pushes to main, git push --no-verify and curl piped into sh; a seatbelt for accidents, not a sandbox](https://github.com/LucasCooperBey/block-destructive) | Copy block-destructive.sh to ~/.claude/hooks and add it as a PreToolUse hook on Bash. |
| 10 | Ecosystem MCP: research npm packages from inside Claude Code | December 8, 2025 | [The repo: research, compare and security-check npm packages from inside Claude Code](https://github.com/SanDiegoAIStudio/ecosystem-mcp) | Add it to Claude Code and ask it to compare two packages before you install either. |
| 11 | TabMap: group 200 open browser tabs by topic | January 13, 2026 | [TabMap, a local Chrome extension and CLI that groups open tabs by topic without sending URLs to a server](https://github.com/LucasCooperBey/tabmap) | Load the unpacked extension in Chrome and group your open tabs by project. |
| 12 | Hooks over reminders: turn CLAUDE.md rules into shell checks | March 8, 2026 | [hook-starter, a pack of Claude Code PreToolUse and PostToolUse shell hooks that enforce rules at tool-call time](https://github.com/LucasCooperBey/hook-starter) | Pick one rule your agent keeps forgetting in CLAUDE.md and wire it as a PreToolUse hook. |
| 13 | Review gate: five checks before a build moves on | February 1, 2026 | [review-gate, a pre-merge checklist and shell runner that blocks a branch until five checks pass](https://github.com/LucasCooperBey/review-gate) | Run review-gate on your current branch before opening a pull request. |
| 14 | ShipGate: scan before a repo goes public | September 29, 2026 | [ShipGate, a one-command pre-flight scanner that checks a repo for secrets, personal paths and git history leaks before it goes public](https://github.com/LucasCooperBey/shipgate) | Clone shipgate and run ./shipgate.sh /path/to/your-repo before flipping a private repo public. |

## Follow along

New doors go up on X every day. This list grows with them.

The machine today, on this Mac: 25 agents, 254 skills, 245 scheduled jobs, 155 that prove their work. Yesterday: 1,297 runs did work, 3,503 had no work, 683 could not; 232 coding-lane runs; 992 commits.

## Follow with your agent

Give your AI assistant this prompt:

```text
Each morning, read today's door at github.com/LucasCooperBey/100-doors. Check whether my setup has this piece. Propose one change I could make, and never install or change anything without asking me first.
```

The opened doors are also here as data: [doors.json](doors.json) and an RSS feed, [feed.xml](feed.xml).

## License

MIT, for everything in this repository.

---

More from me: [sandiegoaiguy.com](https://sandiegoaiguy.com)
