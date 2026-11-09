# Close every chat with a written reason

If you work with AI, you probably end the day with a pile of open chats, terminals and tabs. Each one holds a little state you are afraid to lose, so none of them get closed. The fix is a closing note: before a window goes away, it writes one short note, and the note decides what happens to it.

## The closing note, five lines

```text
WINDOW    What this chat was for, in a few words
VERDICT   close | merge | keep
REASON    One line. Required for every verdict.
CARRY     Where the open work now lives: a task, a file, a successor chat. "Nothing" is allowed for close.
NEXT      The first step for whoever picks it up, or "none"
```

## The three verdicts

- **close**: the work is finished, or written down somewhere else. The window goes.
- **merge**: this chat and another are one piece of work. Both fold into one new chat that starts from both notes.
- **keep**: the window stays open. This is the exception, and its reason must name something a note cannot carry, such as a job still running in it right now, work that is not saved or committed yet, or a login you cannot redo.

Use only these words. A new word, like "keep-ish" or "later", is how windows end up open for a week.

## The rule that makes it work

**No reason, no verdict.** A note with an empty REASON line is rejected and the window stays until someone writes one. That one check is what turns "I'll close it later" into a decision.

## One filled in (made up)

```text
WINDOW    Fixing the signup email template
VERDICT   close
REASON    The fix is merged and the test email arrived
CARRY     Nothing
NEXT      none
```

```text
WINDOW    Pricing page copy, second draft
VERDICT   merge
REASON    Same page as the "pricing table layout" chat; one person should finish both
CARRY     A new chat that starts from both notes
NEXT      Put the new copy into the new table and send it for review
```

## Try it

Before you stop for the day, write the five lines for every chat or terminal you have open. Close everything whose verdict is close. Count how many you were keeping open with no reason you could write down.
