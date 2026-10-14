# Ten moves for your first 30 days building with AI

My first commit message was "initial commit, dude." Five minutes later I made a second one. Everything I have built since sits on top of that habit, so git comes first here. Do one move every three days. Each one has a step you can finish that day.

## 1. Days 1 to 3: learn undo in a practice folder, then commit by name

Undo has to be cheap before anything else, so learn it where nothing can be lost. Make a folder that holds nothing you care about:

```bash
mkdir git-practice && cd git-practice
git init
printf 'first line\n' > notes.txt
git add notes.txt
git commit -m "Add notes"
```

Now break the file and bring it back:

```bash
printf 'a line I did not mean to keep\n' >> notes.txt
git diff notes.txt
git restore notes.txt
cat notes.txt
```

`git diff` shows the change, `git restore notes.txt` puts back the committed version of that one file, and `cat` shows the old text is back.

Then use the same habit in a real project. Run `git status` before each commit, add the files you mean by name, and leave out anything that holds a key, a password or an `.env` file. List those names in `.gitignore` so they never get added. Ask your agent to work the same way: name the files it changed, show you the diff, and commit only those files with a message that says what changed. Done when you have broken a file in the practice folder and watched `git restore` bring the old text back.

## 2. Days 4 to 6: describe the result and leave the steps to the agent

Before you ask for a build, write three lines: what must exist when it is done, who it is for, and what must not be touched. Paste them as your first message. Done when one build went from those three lines with no step-by-step instructions from you.

## 3. Days 7 to 9: ask for a second pass before you look

End your request with: "Review your own work twice, fix what you find, then show me." Done when you have read one fix the agent made on its own review.

## 4. Days 10 to 12: get a second opinion from a different model family

Hand the same change to a model from another company and ask: "What breaks? Name the file and line." Models from one family tend to miss the same things. Done when the second model found something the first one missed, or you have written down that it found nothing.

## 5. Days 13 to 15: keep one page you open every day

One note or one page: what is running, what is waiting on you, what broke. Put it where you already look each morning. Delete any dashboard you stop opening. Done when you have opened it five days in a row.

## 6. Days 16 to 18: give every job three outcomes

Anything that runs without you should end in one of three states: it did the work, there was no work, or it could not run. A job that says nothing when it fails looks the same as a job with nothing to do. Done when one of your jobs reports all three.

## 7. Days 19 to 21: turn real failures into tests

When something breaks, write the check that would have caught it. Then put the bug back on a branch and run the check. If it doesn't go red, it isn't a check yet. Done when one test has failed for the right reason on purpose.

## 8. Days 22 to 24: sort actions by whether you can undo them

Make two lists. Reversible work (edits, branches, drafts) can run on its own. One-way steps (sending, paying, deleting, publishing) wait for your yes, every time. Done when your agent's instructions name both lists.

## 9. Days 25 to 27: close every chat with a written reason

Before you close a session, have it write what it finished, what it verified and how, and what is left. Start the next session by pasting that note in. Done when one session started from the last one's note.

## 10. Days 28 to 30: let the system bring you questions

Ask your setup to end each day with the questions only you can answer, in place of a task list. Widen what it may do alone only where four things exist: a written rule, a check that can say no, proof it worked on the real thing, and an undo you can run in one command. Done when it asked you one question you would not have thought to ask yourself.

## After day 30

Go back to move 1 in your busiest project. Pick one file you changed this month and run `git log --oneline -- path/to/file`. Choose the commit from before the change and read that version with `git show <commit>:path/to/file`. If you can read the old version, you can restore it. If the file has no history, start move 1 again in that project.
