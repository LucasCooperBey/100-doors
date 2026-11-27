# Door 50: I give one tool a repository of its own: a Claude Code skill that runs five yes-or-no checks, scrubs the copy, searches the files, and starts out private

- **Date:** November 26, 2026
- **Built:** November 17, 2026
- **Room:** Tools (4 of 7)
- **Gift:** [opensource](https://github.com/LucasCooperBey/claude-skills/tree/main/skills/opensource)

## What it is

I give one tool a repository of its own. The copy can still carry names from the larger repository. Five yes-or-no checks decide whether it may be public, and an unsure answer means private.

opensource is a Claude Code skill. The scrub and the leak search are Python scripts for any folder, with a sample tool and tests. A replacement that finds nothing fails the scrub. They need Python 3.9 or newer. Git and the GitHub command line tool are only for making the repository, and Claude Code is only for the skill. The repository is created private first, and a public step waits for the owner's yes.

The leak search reads files and not git history, so a history scanner is a separate step.

## Try it today

**The gift:**

[https://github.com/LucasCooperBey/claude-skills/tree/main/skills/opensource](https://github.com/LucasCooperBey/claude-skills/tree/main/skills/opensource)

Clone LucasCooperBey/claude-skills, run mkdir -p ~/.claude/skills, copy skills/opensource into ~/.claude/skills, then from that folder run python3 scripts/leak_search.py leak-terms.example.txt examples/sample-tool and the scrub example in the README. The scripts need Python 3.9 or newer. Git and the GitHub command line tool are only for making a repository, and Claude Code is only for the skill.
100 Doors to Recursion https://github.com/LucasCooperBey/100-doors
