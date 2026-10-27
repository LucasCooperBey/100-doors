# Door 13: Review gate: fresh eyes on every push

- **Date:** October 25, 2026
- **Built:** July 4, 2026
- **Room:** 2
- **Code:** [LucasCooperBey/review-gate](https://github.com/LucasCooperBey/review-gate)

## What it is

Asking the agent that wrote the code to review the code is asking the writer to proofread their own typo. It still remembers why the shortcut felt reasonable ten minutes ago.

Review Gate is a git `pre-push` hook that takes `git diff @{u}..HEAD` and spawns a separate, fresh-context Claude Code process (`claude -p`) with zero session history. It only sees the diff and answers one of three words:

- `PASS`: push goes through.
- `WARN`: push goes through, warning logged.
- `REJECT`: push is blocked with the exact file and line.

Every verdict appends to `~/.ExecutionSpine/ledger.jsonl` so you can audit what was caught before it ever reached a pull request.

## Try it today

Clone [LucasCooperBey/review-gate](https://github.com/LucasCooperBey/review-gate) and run `./install.sh /path/to/your/repo` inside a repo you own to wire the pre-push hook.
