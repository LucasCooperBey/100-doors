# Make an AI draft sound like you

The tool for this door is **writing-check** (https://github.com/LucasCooperBey/writing-check), one Python file with no dependencies. It lists the phrases that make a draft read as machine-written, each with its line and the rule behind it, and gives a weighted rate per 1,000 words. It ships a Claude Code Stop hook, so the model checks its own last reply, and a git pre-commit hook.

## Quick start

```bash
curl -fsSL -o writing_check.py https://raw.githubusercontent.com/LucasCooperBey/writing-check/main/writing_check.py
python3 writing_check.py draft.md
python3 writing_check.py draft.md --max 15   # exit 1 when the rate is over 15 per 1,000 words
```

A checker can flag patterns. It can't decide whether a claim is true or whether a sentence sounds like you, so the method below is still the part only you can do.

## The method behind it

Read the draft aloud. Mark any sentence you wouldn't say to the person reading it.

### Check before you rewrite

- Keep names, dates, prices and other facts unchanged. Check them against your sources.
- Remove claims you can't support. A confident sentence isn't evidence.
- Replace fancy wording with words you'd use in conversation.
- Remove long dashes, repeated points and filler.
- Cut slogans that sound neat but don't explain what happened.
- Explain what the thing is, what it does and what the reader needs to do.
- Keep limitations that affect the reader's decision.

### Paste this under your draft

```text
Rewrite this in plain words I'd say aloud to the reader.
Keep my facts and meaning. Don't add numbers, claims or examples.
Cut filler, repeated points, fancy words and slogans.
Use periods or commas instead of long dashes.
Keep any limits or warnings.
List the changes. Flag claims that need a source and questions you couldn't answer.
```

### Review the result

Compare the rewrite with the original. Check every name, number, date, promise and link. Read it aloud again, and decide for yourself what sounds like you.

A pattern checker can flag wording. It can't prove a claim or guarantee that a rewrite keeps your meaning.
