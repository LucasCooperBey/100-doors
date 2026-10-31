# Door 19: Field Audit: grade your AI setup with receipts

- **Date:** October 30, 2026
- **Built:** July 22, 2026
- **Room:** 2
- **Code:** [LucasCooperBey/intelligent-os-field-audit](https://github.com/LucasCooperBey/intelligent-os-field-audit)

## What it is

Most local business owners know they are losing leads online, but nobody shows them the exact leak in plain English without a 40-page agency pitch.

Field Audit checks a business in 60 seconds and hands back a one-page scorecard with the top three fixes. The open-source harness applies the same method to your AI setup: it is one paste-in prompt (`prompt.md`) that has Claude Code audit the AI system on your machine, scoring 12 parts with a receipt each and naming every gap. It refuses to award a passing score without a file receipt on disk.

## Try it today

**Zero-code prompt (paste your homepage text into ChatGPT or Claude):**

```text
Read my website copy below like a busy local customer on their phone who needs help today. Score it from 0 to 10 on clarity, trust proof, speed to book, and obvious next step, quote the exact line that earned each score, and give me the top 3 fixes I can make in 30 minutes.
```

**Open-source audit harness:**

Clone [LucasCooperBey/intelligent-os-field-audit](https://github.com/LucasCooperBey/intelligent-os-field-audit), paste `prompt.md` into Claude Code at your system root, and post your scorecard as an issue to join the ledger.
