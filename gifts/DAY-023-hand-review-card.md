# The directory and its hand-review card

The directory is live at [directoryofagents.com](https://directoryofagents.com). Open it to compare AI tools by what each one does for you, what it costs one person, how hard it is to set up, and what it is good at and where it falls short. Every listing there is one short card, filled in by hand.

The card below is the shape of every listing, so you can review a tool the directory does not list yet. Fill one in for each tool you are thinking of paying for. Two or three cards side by side usually make the choice.

## The card

```markdown
---
name: The tool's name
tagline: What it does for you, in one line under 120 characters
website: https://the-tool.example
category: the kind of tool, such as coding, workflow automation, voice agents, research, customer support or sales outreach
jobs: [the jobs you would hire it for, such as customer support, bookkeeping, scheduling, email]
pricing: free | freemium | paid
entry_price: the price of the cheapest plan one person can use, or "Pricing not public"
no_code_score: 1 to 5 (1 needs an engineer, 5 is point and click)
setup_time: how long until the first useful result (minutes, an afternoon, days)
best_for_solo: true or false, with the reason in one line
pros:
  - Something specific it does well, that you saw yourself
cons:
  - Something specific that falls short, that you saw yourself
last_tested: YYYY-MM-DD
---

Who it is for, in two or three sentences. Then the honest trade: what you give up, and the one situation where you would pick something else.
```

## Three rules

1. Pros and cons come from your own use. A line you only read on the tool's website goes in the tagline or nowhere.
2. The price is the real one from the tool's pricing page on the day you write the card. When the price sits behind a sales call, write "Pricing not public". Never guess a number.
3. Date the card with the day you last used the tool. Tools change every month, and the date tells you when the card needs another look.

## One filled in (made up)

```markdown
---
name: Example Notetaker (a made-up tool)
tagline: Joins your video calls and sends a summary with action items when the call ends.
website: https://example.com
category: meeting notes
jobs: [scheduling, email]
pricing: freemium
entry_price: "A free plan for a few calls a month, then a paid plan (made up, like the tool)"
no_code_score: 5
setup_time: Minutes
best_for_solo: true
pros:
  - The summary lands right after the call and lists who promised what
  - Connects to a calendar in two clicks, with nothing to configure
cons:
  - Misspells names it has not heard before, so client names need fixing by hand
  - The free plan keeps only recent notes
last_tested: 2026-11-01
---

Good for a one-person business with a handful of client calls a week and follow-ups that slip. If you need notes kept for a year, or your calls are not in English, pick a tool with longer storage and wider language support.
```

## Draft a card with zero code

Paste this into ChatGPT or Claude before you pay for a tool:

"I am deciding whether to pay for [tool]. Fill in this card for it, using only what the tool's own website says today, and write unknown for anything you could not confirm: [paste the card]. Then list three things I should test myself in the first hour."

Then use the tool for that hour and fix the card by hand. The model's draft is where the review starts.
