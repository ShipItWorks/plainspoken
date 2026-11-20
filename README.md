# Plainspoken

You type what you want; it rewrites a prompt an AI understands, then explains changes.

Paused since 18 November 2026, while I finish patchowner. See [patchowner](https://shipitworks.com/patchowner/).

**Score: 67 / 100** on my own [rubric](https://shipitworks.com/how-we-score/). Stage: Beta. Scored 2026-11-12; this record was updated 2026-11-18 from the [product page](https://shipitworks.com/plainspoken/).

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
- e2e and the live OpenRouter rewrite have run logs on main (proof/e2e.log, proof/live-rewrite.log) made at lane commits outside main's history, so they earn nothing here; the live site log (proof/live-site.log, 2026-11-07) recorded /privacy as 404; on 2026-11-18 a review found /privacy on plainspoken.site returning 200 with its full text
- At 847a36d (2026-11-08): no dark mode, and two token pairs measured under 4.5:1 by arithmetic (ink-faint on desk 2.88, pen links 3.98). main at e72687a had a dark colour block (app/globals.css:66); contrast not re-measured in this rescore
- Rate limit is per server instance (in-memory, lost on restart), so it is weak on serverless
- .env.example is stale: it describes per-intent routing and a per-rewrite cost the README says was removed 2026-10-01
- Proof logs for the features are on main since e72687a, but each names a lane commit outside main's history (land PR #72 was a squash merge), and of the seven only proof/e2e.log records an exit code, so none is credited; five of seven are tested with sample data, so they score half
- On 2026-11-08, 64 PRs (6 to 71) were open; most reached main inside land PR #72 as one squash commit, not as merges. On 2026-11-18 gh pr list showed 5 open PRs (#77, #78, #83, #87, #94)
- The repo is private (gh api 2026-11-08), so the live site and the source link cannot be checked by a visitor from this packet; privacy lines stay not yet traced (the full prompt goes to OpenRouter by design)

## What changed

- 2026-11-18: A review corrected two lines here: the privacy page on plainspoken.site now loads (it was a 404 in the 2026-11-07 log), and 5 pull requests are open, not one. No feature label or score changed.
- 2026-11-11: Merged into the product, as the project's changelog and file lists describe it (not run by us): the page now says how many of the hour's tries are left; each rewrite has an "About this rewrite" panel; /api-docs has a "Try it here" part for sending a request from the page; the changelog says every lesson now links its sources; the address that describes the API also reports tries left and where the count is kept. Proof scripts, tests and an audit document were also added. We did not run any of this in a browser, so no feature label or score changed (PRs #79, #81, #80, #76, #85, #86, #84, #82 and #74). Scorecard rows: "Rate limit 15/hour/IP" (works true, Tested with sample data) for the tries count, "Lessons (/learn, 9 paths) with sources" (works true, Tested with sample data) for the lesson sources, and the browser UI row (works false, Not tested yet) as the nearest row to the page changes; the "About this rewrite" panel and the "Try it here" API part are not scored (no row covers them).
- 2026-11-11: Merged into the product: changes to the rewrite and fill-in-the-blanks code, and a shared store for the limit on tries. Not run in a browser by us; no feature label or score changed (PRs #75 and #73).
- 2026-11-10: Site copy only: a dated correction now sits under the demo video for the narration line at 1:06. No code or score change.
- 2026-11-10: Land PR #72 merged into main as e72687a (merge of 3 lane PRs: #71, #10 and #9; #71 carried 60 more); no feature label changed this round. Tagged v0.3.0 at e72687a.
- 2026-11-08: Re-scored against main (847a36d, tag v0.2.0): 67/100 on our own rubric, down from 75. Feature points now follow the proof rule: 25 points over 7 features, half for tested with sample data, none have a proof log on main. Tests on main are 50 passing (CI run 42485460787), not the 70 measured on an unmerged branch.

See [CHANGELOG](CHANGELOG.md).

## Demo

[Transcript of the demo (2:07)](https://shipitworks.com/plainspoken/transcript/) · video on the [product page](https://shipitworks.com/plainspoken/)

The demo voice is AI-generated (ElevenLabs, "Bella") and the demo shows made-up data. The video says so at the end.

## Source code

The source is private for now. This repository holds the public record for the product: this README and a CHANGELOG, and soon a LICENSE. Until the source is public, the [product page](https://shipitworks.com/plainspoken/) is the source of truth, and the score above is the one to trust.

## How I work

I say only what I can back. I say what is not finished before anyone asks. I name people, companies and tools to give credit. I collect as little data as possible. Built with Claude, by Anthropic: Claude helps write the code and wrote this README. Directed, tested and owned by Robert Sweetman in Stoughton, Massachusetts.

Full version: [github.com/ShipItWorks](https://github.com/ShipItWorks) · Contact: support@shipitworks.com

---

Drafted with Claude (Anthropic) from the product page on 2026-11-02. Owner review by Robert Sweetman: pending.
