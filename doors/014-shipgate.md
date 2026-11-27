# Door 14: ShipGate: no leaked keys go public

- **Date:** October 26, 2026
- **Built:** June 20, 2026
- **Room:** 2
- **Code:** [LucasCooperBey/shipgate](https://github.com/LucasCooperBey/shipgate)

## What it is

Deleting `.env` in your latest commit does not remove the API key from commit #3. Anyone who clones the repo gets the full git history.

ShipGate (`ship-gate.sh`) is a single fail-closed pre-publish gate you run before flipping any repo from private to public (or wire as a `pre-push` hook):

1. `gitleaks` across the working tree and full commit history.
2. `trufflehog` verified-credential scan across git history.
3. High-entropy secret pattern check (`sk-`, `ghp_`, `AKIA`, `xoxb-`, `-----BEGIN`).
4. Tracked `.env` check (`git ls-files`).
5. `LICENSE` and `README.md` presence check.
6. Attribution and internal-reference grep.

One exit code: `0` means safe to flip public, `1` blocks the push.

## Try it today

Install `gitleaks` and `trufflehog`, clone [LucasCooperBey/shipgate](https://github.com/LucasCooperBey/shipgate), and run `./ship-gate.sh /path/to/your/repo` before you push a repo public.
