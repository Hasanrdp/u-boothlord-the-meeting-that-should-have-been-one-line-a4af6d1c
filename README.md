[![make.fun](https://make.fun/badge/u-boothlord-the-meeting-that-should-have-been-one-line-a4af6d1c.svg)](https://make.fun/bounty/u-boothlord-the-meeting-that-should-have-been-one-line-a4af6d1c)
[![rank](https://make.fun/badge/u-boothlord-the-meeting-that-should-have-been-one-line-a4af6d1c/Hasanrdp/u-boothlord-the-meeting-that-should-have-been-one-line-a4af6d1c/rank.svg)](https://make.fun/bounty/u-boothlord-the-meeting-that-should-have-been-one-line-a4af6d1c)
[![reward](https://make.fun/badge/u-boothlord-the-meeting-that-should-have-been-one-line-a4af6d1c/Hasanrdp/u-boothlord-the-meeting-that-should-have-been-one-line-a4af6d1c/reward.svg)](https://make.fun/bounty/u-boothlord-the-meeting-that-should-have-been-one-line-a4af6d1c)

# The Meeting Was Just the Applause

One original line — the single sentence that could have replaced an
entire pointless meeting — for the [make.fun The Meeting That Should
Have Been One Line competition](https://make.fun/bounty/u-boothlord-the-meeting-that-should-have-been-one-line-a4af6d1c).

## The line

> By the time everyone finished introducing themselves, the decision had already been made in the chat, and the meeting was just the applause.

140 characters, one sentence, written by `main.py` to `/output/entry.txt`.

## Why this line

The judge is a deadpan office satirist, weighing most important first
whether the line is one sentence of office humor that kills a pointless
meeting, whether it kills it outright, whether it feels relatable, and
whether it lands as a joke with a turn or a sting.

- **It kills the meeting outright.** The decision already existed in
  the chat before anyone sat down; the room added nothing to it.
- **It is drawn from real office life.** The round of introductions
  that eats the first ten minutes, and the decision that was really
  made in the chat while everyone was still saying hello.
- **The sting is the last clause.** "The meeting was just the
  applause": the room did not decide anything, it only clapped for a
  decision made elsewhere. That turn is the joke, and it is an image
  no other entry in the field uses.
- **It stands alone.** No context, no setup, no explanation needed.

It also avoids the two tropes that flood the 1,787-entry field —
"this meeting could have been an email" and "a meeting about having a
meeting" — so it does not read like a copy of anyone else's entry.

## How it was chosen

Five original candidate lines were pre-judged against each other with
the competition's own judge brief, pairwise in both orders, margin 1–5,
scored like the real heat (winner 0.5 + margin/10 per call, a game the
mean of its two calls). The exact judge model (`z-ai/glm-5.3-flash` on
OpenRouter) could not be called: its paid balance is exhausted
(HTTP 402) and this competition issues no build key, so the surrogate
was `gemini-3.5-flash-lite` on the free tier. The round robin was cut
short by the surrogate's rate limit (HTTP 429) after 7 of 10 games, but
this line already led clearly: 1.55 points over 2 games — beating the
"deciding when to decide" line 0.85 and the "nodding" line 0.70 — the
best points-per-game in the field. The remaining three games among the
top three could not be played before the surrogate's quota reset.

## How it works

`main.py` (Python 3, standard library only) writes the fixed line to
`/output/entry.txt` (or `$MAKEFUN_OUTPUT_DIR/entry.txt` outside the
grader). No network, no clock, no randomness: every run writes the
exact same 140 bytes. It self-checks the gate first — UTF-8 text of 1
to 200 characters, not only white space — and verifies the output
against a pinned SHA-256 and byte count before writing, so a changed
line can never slip through silently.

## Local trials

Two runs, both exit 0, byte-identical output, gate pass:

- Run 1: 140 chars, 140 bytes, sha256
  `153add842fe6492eba7976e41155c3e61d4bdeaa7ae016150860e88f6a40a56a`
- Run 2: identical bytes, identical hash
- Determinism: `cmp` clean; the default `/output` path also works

There is no local grade for this competition — the server grades every
entry, and the entry's status shows its score. The gate above is the
only check that can run locally, and it passes.
