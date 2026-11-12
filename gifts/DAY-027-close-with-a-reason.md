# Close every chat with a written reason

The tool for this door is **closeout**: https://github.com/LucasCooperBey/close-with-a-reason

It reads the Claude Code transcripts on your machine (and Codex CLI sessions in the same format), writes a short closing note for each recent chat, and sorts the chats into safe to close, keep open, and merge. A chat with an uncommitted or untracked file, an unpushed commit, or a request with no answer stays open, and its note names what is still unsaved.

## Quick start

Python 3.9 or newer, nothing to install:

```bash
curl -fsSL -o closeout.py https://raw.githubusercontent.com/LucasCooperBey/close-with-a-reason/main/closeout.py
python3 closeout.py list
python3 closeout.py sweep
```

`list` prints the three groups and writes nothing. `sweep` writes one note per chat plus an `INDEX.md` into `~/closeouts/YYYY-MM-DD`. Nothing leaves your machine unless you pass `--provider` to have a model write the NEXT line, and then only that chat's last 12 typed turns go to it. The repo also installs as a Claude Code skill.

## The method behind it

If you work with AI, you probably end the day with a pile of open chats, terminals and tabs. Each one holds a little state you are afraid to lose, so none of them get closed. The fix is a closing note: before a window goes away, it writes one short note, and the note decides what happens to it.

### The closing note, five lines

```text
WINDOW    What this chat was for, in a few words
VERDICT   close | merge | keep
REASON    One line. Required for every verdict.
CARRY     Where the open work now lives: a task, a file, a successor chat. "Nothing" is allowed for close.
NEXT      The first step for whoever picks it up, or "none"
```

### The three verdicts

- **close**: the work is finished, or written down somewhere else. The window goes.
- **merge**: this chat and another are one piece of work. Both fold into one new chat that starts from both notes.
- **keep**: the window stays open. This is the exception, and its reason must name something a note cannot carry, such as a job still running in it right now, work that is not saved or committed yet, or a login you cannot redo.

Use only these words. A new word, like "keep-ish" or "later", is how windows end up open for a week.

### The rule that makes it work

**No reason, no verdict.** A note with an empty REASON line is rejected and the window stays until someone writes one. That one check is what turns "I'll close it later" into a decision.

### One filled in (made up)

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

### Try it

Before you stop for the day, write the five lines for every chat or terminal you have open. Close everything whose verdict is close. Count how many you were keeping open with no reason you could write down.
