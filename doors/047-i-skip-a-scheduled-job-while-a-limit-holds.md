# Door 47: I skip a scheduled job while a limit holds: a wrapped job skips until the reset the tool reads in the notice, or for a window of hours when it reads none

- **Date:** November 25, 2026
- **Built:** November 14, 2026
- **Room:** 5
- **Gift:** [max-pool-governor](https://github.com/SanDiegoAIStudio/max-pool-governor)

## What it is

I skip a scheduled job while a limit holds. Unattended jobs keep launching on an exhausted plan. A wrapped job can skip until the reset the tool reads in the notice, or for a window of hours when it reads none.

max-pool-governor is a small Python program that uses only the standard library. It needs Python 3.9 or later because it imports zoneinfo, and it does not run on Windows. It reads only the notice it is shown. A line with no reset time lasts the default window of 24 hours. A job you do not wrap is invisible to it.

It sets no order among jobs, and a job is guarded only when its own wrapper checks the flag before it runs.

## Try it today

**The gift:**

[https://github.com/SanDiegoAIStudio/max-pool-governor](https://github.com/SanDiegoAIStudio/max-pool-governor)

Clone SanDiegoAIStudio/max-pool-governor, run python3 -m unittest discover -s tests -q, then MAX_POOL_STATE_DIR=$(mktemp -d) sh examples/nightly.sh. The sample needs no account.
100 Doors to Recursion https://github.com/LucasCooperBey/100-doors
