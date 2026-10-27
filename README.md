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
| 11 | TabMap: why 200 tabs are open | December 30, 2025 | [TabMap: captures your open tabs, labels each by intent, project, stale or solved, then offers a cleanup that lists before it closes anything](https://github.com/LucasCooperBey/tabmap) | Clone it, pip install -r requirements.txt, run python3 -m tab_intel.capture, then preview the cleanup with auto_cleaner.py --dry-run. |
| 12 | Hooks over reminders: checks on every agent edit | January 30, 2026 | [harness-guard: four quality hooks plus the safety hooks for Claude Code, each a short shell script you can read first](https://github.com/LucasCooperBey/harness-guard) | Clone it and run ./install.sh, or merge just the four quality-hook lines from settings.example.json into ~/.claude/settings.json. |
| 13 | Review gate: fresh eyes on every push | July 4, 2026 | [review-gate: one Python file (standard library only), an install script that writes a pre-push hook, and 24 tests](https://github.com/LucasCooperBey/review-gate) | Run install.sh inside your project to add the pre-push hook; it needs the Claude Code CLI signed in and Python 3.10 or newer. |
| 14 | ShipGate: no leaked keys go public | June 20, 2026 | [ShipGate: one shell script, ship-gate.sh, that runs gitleaks and trufflehog over the full history and checks the LICENSE, a raw .env and attribution, with one exit code](https://github.com/LucasCooperBey/shipgate) | brew install gitleaks trufflehog, put ship-gate.sh on your PATH and run it in a repo before it goes public. |
| 15 | Changelog Digest: your changelog becomes content | December 4, 2025 | [changelog-digest again (the Door 8 tool): a Python script that reads a markdown changelog and writes a hook, a short story and video ideas](https://github.com/SanDiegoAIStudio/changelog-digest) | Run python3 changelog_digest.py examples/sample-changelog.md --date 2026-03-14 --dry-run to see the prompt without an API key. |

## Follow along

New doors go up on X every day. This list grows with them.

The machine today, on this Mac: 25 agents, 254 skills, 250 scheduled jobs, 160 that prove their work. Yesterday: 1,256 runs did work, 3,515 had no work, 492 could not; 17 coding-lane runs; 252 commits.

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
