# Door 15: Changelog Digest: your changelog becomes content

- **Date:** October 27, 2026
- **Built:** December 4, 2025
- **Room:** 2
- **Code:** [SanDiegoAIStudio/changelog-digest](https://github.com/SanDiegoAIStudio/changelog-digest)

## What it is

You already write down what you built each day. changelog-digest turns that log into something you can post.

It reads a local markdown changelog, keeps the entries for one day (or the seven days ending on a date with `--week`), and asks a Claude model for a digest with a hook, the story, breakthroughs, challenges, what is next, and video ideas.

- `--dry-run` prints the prompt and skips the model call, so you can see exactly what would be sent.
- `--out-dir DIR` saves the digest as `DIR/YYYY-MM-DD-digest.md`.
- Files Modified sections are never sent to the model.

## Try it today

Clone [SanDiegoAIStudio/changelog-digest](https://github.com/SanDiegoAIStudio/changelog-digest) and run the dry run on the sample changelog, then on your own:

```bash
python3 changelog_digest.py examples/sample-changelog.md --date 2026-03-14 --dry-run
```

A real run needs `ANTHROPIC_API_KEY`.
