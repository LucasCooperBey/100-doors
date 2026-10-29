# Door 17: Blind Council: five models argue, one settles

- **Date:** October 29, 2026
- **Built:** July 9, 2026
- **Room:** 2
- **Code:** [LucasCooperBey/blind-council](https://github.com/LucasCooperBey/blind-council)

## What it is

Ask one AI a hard question and it agrees with your framing. Put five models in a shared chat and the second agrees with the first.

Blind Council gives you an adversarial second opinion before you make a high-stakes call:

1. Five frontier models answer your question independently in parallel.
2. Each model cross-examines the other four under shuffled anonymous labels (`MEMBER-A` through `MEMBER-E`) so none of them can defer to brand name or majority.
3. A sixth synthesizer model that never took a side reads the blind answers and critiques and writes the final verdict, where the council agreed, and the strongest surviving dissent.

## Try it today

**Zero-code prompt (paste into ChatGPT or Claude):**

```text
Don't just give me one answer. Run a 3-seat Blind Council on this decision: Seat A (The Pragmatist), Seat B (The Skeptic), and Seat C (The First-Principles Operator). First, write each seat's independent answer. Second, have each seat ruthlessly critique the weak assumptions in the other two. Finally, step in as an impartial Judge who never took a side and give me the final verdict + the strongest surviving dissent.
```

**Open-source CLI:**

Clone [LucasCooperBey/blind-council](https://github.com/LucasCooperBey/blind-council), add `OPENROUTER_API_KEY` to `.env`, and run:

```bash
bun install
bun run council "your question"
```
