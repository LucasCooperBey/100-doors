# Review with a different model family

When a model writes code and another copy of the same model reviews it, they tend to share the same blind spots. A reviewer trained by a different company asks different questions. In one case, three reviewers from the same family passed a scheduled job, and a reviewer from another family found the bug they missed: a run that had died would have reported the previous run's result as a fresh success.

## The checklist

1. **Hand over the change, not the story.** Give the second model the diff and the tests, plus one line on what the change is meant to do. Leave out your own explanation of why it is right.
2. **Ask what breaks.** "List the ways this fails in production. For each, name the input and what goes wrong." Do not ask "is this good?"
3. **Fix what is real.** For each finding, either fix it with a test that fails before the fix, or write one line on why it is not a bug.
4. **Run it again.** Send the new diff back. Each round tends to find what the last round could not see.
5. **Stop at a cap you set before you start.** Two or three rounds is a sensible cap. Stop there even if it still finds small things, and write down what is left.

## What to paste

```text
Here is a diff and its tests. The change is meant to: <one line>.
List every way this could fail in real use. For each one, give the input
that triggers it, what goes wrong, and the smallest fix. Do not praise
the code. If you find nothing, say what you checked.
```

## Try it

Take the last change an AI wrote for you. If Claude wrote it, review it with a model from another company, or the other way round. Paste the prompt above, and count how many findings are real.
