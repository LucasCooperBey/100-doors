# Door 20: Precompact Protector: keep your place through a compaction

- **Date:** October 30, 2026
- **Built:** June 17, 2026
- **Room:** 2
- **Code:** [LucasCooperBey/precompact-protector](https://github.com/LucasCooperBey/precompact-protector)

## What it is

Nothing kills momentum faster than a two-hour AI chat resetting right when you are about to finish, forcing you to re-explain the whole project from scratch.

Precompact Protector is two Claude Code hooks. The PreCompact hook saves the last 40 user and assistant turns to a private checkpoint on your own disk before Claude Code compacts. The SessionStart hook (matcher `compact`) prints a short card when the session wakes up: your last request, up to 8 files in play and the checkpoint time, plus an optional `REHYDRATE.md` your own summarizer writes. Python 3.9 or newer, standard library only, MIT.

## Try it today

**Zero-code prompt (paste into ChatGPT or Claude before your thread gets long):**

```text
Write a compact 10-line Handoff Card of our session so far: list the exact goal, every locked decision we made, what we rejected and why, and the single next step I should paste into a fresh chat.
```

**Open-source hooks:**

Clone [LucasCooperBey/precompact-protector](https://github.com/LucasCooperBey/precompact-protector) and merge `settings-snippet.json` into `~/.claude/settings.json` with the real path; nothing to install. Run the tests with:

```bash
python3 -m unittest discover -s tests
```
