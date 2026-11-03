# Plainspoken

You type what you want; it rewrites a prompt an AI understands, then explains the changes.

**Score: 75 / 100** on the [ShipItWorks rubric](https://shipitworks.com/how-we-score/). Stage: Beta. As of 2026-11-02, from the [product page](https://shipitworks.com/apps/#plainspoken).

Every number on the product page names the file it came from. The lists below are copied from that page, not rewritten.

**Platform.** Web only.

## What works today

- Prompt validation (3-2000 chars, intent hint)
- Rate limit 15/hour/IP
- Fill-in blanks + free self-check
- Lessons (/learn, 9 paths) with sources

## Not done yet

- e2e never run here (missing Chromium build); the live OpenRouter rewrite path and the live site have never been seen working
- No dark mode; two token pairs measure under 4.5:1 by arithmetic
- Rate limit is per server instance (in-memory, lost on restart), so it is weak on serverless
- .env.example is stale: it describes per-intent routing and a per-rewrite cost the README says was removed 2026-10-01

## Demo

[Transcript of the demo (1:40)](https://shipitworks.com/plainspoken/transcript/) · video on the [product page](https://shipitworks.com/apps/#plainspoken)

The demo voice is AI-generated (ElevenLabs, "Alice") and the demo shows made-up data. The video says so at the end.

## Source code

The source is private for now. This repository holds the public record for the product: this README, and soon a CHANGELOG and LICENSE. Until the source is public, the [product page](https://shipitworks.com/apps/#plainspoken) is the source of truth, and the score above is the one to trust.

## How we work

Say only what we can back. Say what is not finished before anyone asks. Name people, companies and tools to give credit. Collect as little data as possible. We use AI and say so: Claude (by Anthropic) helps write the code and wrote this README.

Full version: [github.com/ShipItWorks](https://github.com/ShipItWorks) · Contact: support@shipitworks.com

---

Drafted with Claude (Anthropic) from the product page on 2026-11-02 and reviewed by Robert Sweetman.
