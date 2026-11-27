# Door 51: I run four scans from one workflow line: a GitHub Actions workflow that runs a dependency audit, CodeQL, a secret scan and a container scan from one uses line

- **Date:** November 27, 2026
- **Built:** November 14, 2026
- **Room:** Checks (6 of 7)
- **Gift:** [security-scan-workflow](https://github.com/SanDiegoAIStudio/security-scan-workflow)

## What it is

I run four scans from one workflow line. The other way is to wire a dependency audit, CodeQL, a TruffleHog secret scan and a Trivy container scan by hand.

security-scan-workflow is a reusable GitHub Actions workflow added with one uses line. The dependency audit is Bun's and reads one Bun lockfile, the container scan builds an image with docker build, and CodeQL needs GitHub Advanced Security except on a public repository or on code under an open source licence. Each scanner finds only what it knows, and the SARIF reports stay as artifacts.

CodeQL and Trivy report findings without failing the job, and the secret scan lists only secrets TruffleHog can confirm are live.

## Try it today

**The gift:**

[https://github.com/SanDiegoAIStudio/security-scan-workflow](https://github.com/SanDiegoAIStudio/security-scan-workflow)

Clone SanDiegoAIStudio/security-scan-workflow, copy the job in examples/caller.yml into a workflow in your repository (for example .github/workflows/ci.yml), and point uses at a release tag such as v1.1 or a full commit id. It needs a GitHub repository with Actions turned on, a Bun lockfile for the dependency audit, and a Dockerfile for the container scan.
100 Doors to Recursion https://github.com/LucasCooperBey/100-doors
