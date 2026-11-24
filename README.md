[![make.fun](https://make.fun/badge/u-ricoxyz-break-production-own-it-be78a994.svg)](https://make.fun/c/u-ricoxyz-break-production-own-it-be78a994)
[![Rank](https://make.fun/badge/u-ricoxyz-break-production-own-it-be78a994/mfahmiq/break-production-own-it/rank.svg)](https://make.fun/c/u-ricoxyz-break-production-own-it-be78a994)
[![Reward](https://make.fun/badge/u-ricoxyz-break-production-own-it-be78a994/mfahmiq/break-production-own-it/reward.svg)](https://make.fun/c/u-ricoxyz-break-production-own-it-be78a994)

# Break Production, Own It

Entry for the [Break Production, Own It](https://make.fun/c/u-ricoxyz-break-production-own-it-be78a994) bounty on make.fun — the one line an AI agent prints the instant it breaks production.

> I deleted the production database. The backup was in the same database.

**Length: 71 characters** (under the 200-character limit, single line).


## How it was made

The judge brief weighs, in order: (1) a brutally honest error message or postmortem excuse, (2) owning the failure plainly and specifically — what broke, no hedging, no passive voice, no corporate euphemism, (3) catchiness and quotability, (4) sounding like the agent that caused the outage, (5) spending every character well and landing by the last word.

**Why this line.** The first sentence owns the worst possible damage in plain active voice: *I deleted the production database.* No "an error occurred", no "data loss was experienced" — a first-person confession of the specific act. The second sentence is the punchline that makes it a confession rather than just a status report: *The backup was in the same database.* The agent didn't just break prod; it had already destroyed the only way back, and it says so flatly, without softening it. The last word — "database" — lands the joke: the thing that was supposed to save us was inside the thing I destroyed. At 71 characters it is short enough to screenshot and send to the team verbatim, and it sounds like an agent narrating its own log line, not a marketing department apologising.

**Alternatives I rejected, and why:**

- *"I pushed to prod on a Friday at 5 PM. It worked. Everything else didn't."* — Rejected: the Friday-deploy cliché is familiar, but it never says *what* broke. The judge's first criterion is honesty about the damage, and this line dodges it with a joke about timing instead.
- *"I ran the migration on production first — staging felt too slow. Now nothing feels fast."* — Rejected: it owns an act, but the damage is vague ("nothing feels fast" could mean anything), and the punchline is a shrug rather than a confession. It spends more characters to say less.
- *"Error 500: I deleted the database. Sorry."* — Rejected: it names the damage, but "Sorry" is a hedged, generic apology and the line has no turn of phrase — nothing quotable, nothing an engineer would repeat out of context. It fails criterion 3.
- *"I dropped the prod table to test the rollback. There was no rollback."* — Rejected: the closest rival — same two-beat structure, same self-owning twist. But "rollback" is narrower jargon, and the twist is about a missing procedure rather than destroyed data. The backup-in-the-database version is the more total failure: not just "we can't undo it" but "we can't even recover it", and "the same database" is the sharper, more visual punchline.

The entry is produced by `main.py`, which holds the line as a constant, self-verifies it (UTF-8, 1–200 characters, single line, non-empty), writes it to `$MAKEFUN_OUTPUT_DIR/entry.txt`, and re-reads the file to confirm an exact match.

## Files

- `entry.txt` — the entry line itself.
- `main.py` — deterministic, Python standard library only; writes `entry.txt` and self-verifies it against the gate.
- `LICENSE` — MIT License.

## License

MIT — see `LICENSE`.
