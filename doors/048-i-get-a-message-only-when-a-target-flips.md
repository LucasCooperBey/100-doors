# Door 48: I get a message only when a target flips: a Cloudflare Worker that checks the addresses you list, records heartbeats, and sends a Telegram message only when one flips between up and down

- **Date:** November 25, 2026
- **Built:** November 13, 2026
- **Room:** Agents (5 of 7)
- **Gift:** [fleet-canary](https://github.com/SanDiegoAIStudio/fleet-canary)

## What it is

I get a message only when a target flips. A note on every check is noise. A machine that has never reported a heartbeat stays unknown and does not raise an alert.

fleet-canary is a Cloudflare Worker. Once deployed, it checks the addresses you list every five minutes and records heartbeats from your machines. It needs Bun, Node.js 22 or newer, and curl for a local run, and a Cloudflare account and a Telegram bot to deploy it and get alerts. With no Cloudflare account and no Telegram bot, a local run still checks and records a heartbeat, and no message is sent.

The status page and GET /status do not check the shared secret, so anyone with the Worker's address can read the target states.

## Try it today

**The gift:**

[https://github.com/SanDiegoAIStudio/fleet-canary](https://github.com/SanDiegoAIStudio/fleet-canary)

Clone SanDiegoAIStudio/fleet-canary, run bun install, bun test and bun run typecheck, copy .dev.vars.example to .dev.vars, start the local server with bun run dev, then curl -sS http://localhost:8787/__scheduled. A local run needs no Cloudflare account and sends no Telegram message.
100 Doors to Recursion https://github.com/LucasCooperBey/100-doors
