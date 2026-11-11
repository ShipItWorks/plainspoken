# Plainspoken

You type what you want; it rewrites a prompt an AI understands, then explains changes.

**Score: 67 / 100** on our own [rubric](https://shipitworks.com/how-we-score/). Stage: Beta. Scored 2026-11-10; this record was updated 2026-11-10 from the [product page](https://shipitworks.com/apps/#plainspoken).

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
- e2e and the live OpenRouter rewrite have run logs on main (proof/e2e.log, proof/live-rewrite.log) made at lane commits outside main's history, so they earn nothing here; the live site log (proof/live-site.log, 2026-11-07) records a FAIL: /privacy 404
- At 847a36d (2026-11-08): no dark mode, and two token pairs measured under 4.5:1 by arithmetic (ink-faint on desk 2.88, pen links 3.98). main now has a dark colour block (app/globals.css:66); contrast not re-measured in this rescore
- Rate limit is per server instance (in-memory, lost on restart), so it is weak on serverless
- .env.example is stale: it describes per-intent routing and a per-rewrite cost the README says was removed 2026-10-01
- Proof logs for the features are on main since e72687a, but each names a lane commit outside main's history (land PR #72 was a squash merge), and of the seven only proof/e2e.log records an exit code, so none is credited; five of seven are tested with sample data, so they score half
- On 2026-11-08, 64 PRs (6 to 71) were open. On 2026-11-10 gh pr list shows one open PR (#6, not on main); the rest reached main inside land PR #72 as one squash commit, not as merges
- The repo is private (gh api 2026-11-08), so the live site and the source link cannot be checked by a visitor from this packet; privacy lines stay not yet traced (the full prompt goes to OpenRouter by design)

## What changed

- 2026-11-10: Site copy only: a dated correction now sits under the demo video for the narration line at 1:06. No code or score change.
- 2026-11-10: Land PR #72 merged into main as e72687a (merge of 3 lane PRs: #71, #10 and #9; #71 carried 60 more); no feature label changed this round. Tagged v0.3.0 at e72687a.
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
