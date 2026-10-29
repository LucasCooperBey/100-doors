# Door 18: The Spine Pattern: memory that never erases

- **Date:** October 30, 2026
- **Built:** June 18, 2026
- **Room:** 2
- **Code:** [LucasCooperBey/spine-pattern](https://github.com/LucasCooperBey/spine-pattern)

## What it is

Most AI memory tools overwrite old facts in place when your plans change, silently erasing what you decided earlier and why.

The Spine Pattern stores every change as a dated line in an append-only plain-text log (`spine.jsonl`) with provenance (`source`, `agent`, `timestamp`) and typed `SUPERSEDES` edges. Every database table, search index, or summary view is a disposable projection that can be rebuilt from the spine in seconds.

## Try it today

**Zero-code prompt (paste into ChatGPT or Claude):**

```text
From now on, keep a dated Decision Log at the bottom of our chat. Never overwrite or delete an old rule when my plans change: instead, add a new dated line showing what we decided, what it replaced, and why.
```

**Open-source reference engine (Python standard library only):**

Clone [LucasCooperBey/spine-pattern](https://github.com/LucasCooperBey/spine-pattern) and run the test suite and ledger walkthrough:

```bash
python3 -m unittest discover -s tests -v
```
