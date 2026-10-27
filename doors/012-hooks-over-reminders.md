# Door 12: Hooks over reminders: checks on every agent edit

- **Date:** October 24, 2026
- **Built:** January 30, 2026
- **Room:** 2
- **Code:** [LucasCooperBey/harness-guard](https://github.com/LucasCooperBey/harness-guard)
- **Gift:** [gifts/DAY-012-pre-commit-hook.md](../gifts/DAY-012-pre-commit-hook.md)

## What it is

Your agent reads `CLAUDE.md` at 9am and forgets it by 9:20. Around tool call 40, the rules at the top of the prompt start losing to the last ten errors in the window.

`CLAUDE.md` is a wish. A hook is a law.

Instead of reminding the agent not to leave debug logs, secrets, or type errors behind, wire four small post-edit and pre-commit hooks into `~/.claude/settings.json` so every edit runs through deterministic shell checks automatically.

## The four quality hooks

1. Format on save (`prettier` or `ruff` on the touched file).
2. TypeScript check on `.ts` and `.tsx` edits (`tsc --noEmit`).
3. Debug-statement warning on `console.log` in edited lines.
4. Secret scan before commit (`gitleaks` or `trufflehog`).

## Try it today

Add one post-edit hook in `~/.claude/settings.json` from [LucasCooperBey/harness-guard](https://github.com/LucasCooperBey/harness-guard) or [gifts/DAY-012-pre-commit-hook.md](../gifts/DAY-012-pre-commit-hook.md) and make a test edit with a `console.log` to watch it catch it.
