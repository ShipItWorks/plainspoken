# Plainspoken

You type what you want; it rewrites a prompt an AI understands, then explains changes.

**Score: 67 / 100** on our own [rubric](https://shipitworks.com/how-we-score/). Stage: Beta. Scored 2026-11-08; this record was updated 2026-11-08 from the [product page](https://shipitworks.com/apps/#plainspoken).

Every number on the product page names the file it came from. The lists below are copied from that page, not rewritten.

**Platform.** Web only.

## What works today

- Prompt validation (3-2000 chars, intent hint) (Tested with sample data)
- Rewrite via OpenRouter claude-haiku-4.5 with zdr + data_collection deny (Tested with sample data)
- Rate limit 15/hour/IP (Tested with sample data)
- Fill-in blanks + free self-check (Tested with sample data)
- Lessons (/learn, 9 paths) with sources (Tested with sample data)

## Not done yet

- Browser UI end to end (e2e, desktop + mobile) (Not tested yet)
- Live site plainspoken.site (Not tested yet)
- e2e not run here (missing Chromium build); the live OpenRouter rewrite path and the live site have not been seen working
- No dark mode; two token pairs measure under 4.5:1 by arithmetic (ink-faint on desk 2.88, pen links 3.98), not yet fixed
- Rate limit is per server instance (in-memory, lost on restart), so it is weak on serverless
- .env.example is stale: it describes per-intent routing and a per-rewrite cost the README says was removed 2026-10-01
- No proof log for any feature on the main branch; five of seven are tested with sample data only, so they score half
- 64 open PRs (numbers 6 to 71, gh pr list 2026-11-08) are open and not merged to main; the privacy page, changelog and four test files from the audited branch are not on main
- The repo is private (gh api 2026-11-08), so the live site and the source link cannot be checked by a visitor from this packet; privacy lines stay not yet traced (the full prompt goes to OpenRouter by design)

## What changed

- 2026-11-08: Re-scored against main (847a36d, tag v0.2.0): 67/100 on our own rubric, down from 75. Feature points now follow the proof rule: 25 points over 7 features, half for tested with sample data, none have a proof log on main. Tests on main are 50 passing (CI run 42485460787), not the 70 measured on an unmerged branch.
- 2026-11-08: PR #64 merged: CI runs on the self-hosted runner; run 42485460787 on main is green. Tag v0.2.0. The build lane's open PRs (6 to 71) are not merged and earn nothing here.

See [CHANGELOG](CHANGELOG.md).

## Demo

[Transcript of the demo (1:40)](https://shipitworks.com/plainspoken/transcript/) · video on the [product page](https://shipitworks.com/apps/#plainspoken)

The demo voice is AI-generated (ElevenLabs, "Alice") and the demo shows made-up data. The video says so at the end.

## Source code

The source is private for now. This repository holds the public record for the product: this README and a CHANGELOG, and soon a LICENSE. Until the source is public, the [product page](https://shipitworks.com/apps/#plainspoken) is the source of truth, and the score above is the one to trust.

## How we work

Say only what we can back. Say what is not finished before anyone asks. Name people, companies and tools to give credit. Collect as little data as possible. We use AI and say so: Claude (by Anthropic) helps write the code and wrote this README.

Full version: [github.com/ShipItWorks](https://github.com/ShipItWorks) · Contact: support@shipitworks.com

---

Drafted with Claude (Anthropic) from the product page on 2026-11-02. Owner review by Robert Sweetman: pending.
