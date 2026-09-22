---
name: checkup
description: A short conversation that keeps this OS's knowledge true. Reads knowledge/, picks the oldest-unconfirmed and most load-bearing beliefs, and asks the owner to confirm, correct, or reject each one. Use for /checkup, or when the audit flags knowledge as overdue. Five minutes, never an interrogation.
---

# Checkup — is what I believe still true?

Onboarding must never be the only day this system learns the business.
Businesses change; a system running on last quarter's facts recommends
wrong things. The checkup is the standing cure for drift.

## Steps

1. Read the fact files in knowledge/ (business profile, owner profile,
   voice, priorities — not reference docs). Rank their claims by two
   things: age (the "Last confirmed" date — a missing date counts as
   oldest) and weight (facts other work depends on: the team, the offers,
   the clients, the prices, the priorities).
2. Pick the top five to eight claims. Never the whole base — this is five
   minutes, not an interrogation.
3. Ask conversationally, one at a time: state the belief plainly and let
   the owner confirm, correct, or reject. *"I believe you have nine
   clients and two offers, and that Jerome runs the ad accounts — still
   true?"* File each answer as it lands: corrections written into the
   file, rejections removed (logged in decisions.md if meaningful),
   confirmations refresh the file's "Last confirmed" date.
4. Anything newly learned mid-checkup follows the capture rules: stated
   facts file immediately; inferences ask.
5. Close in one line: what was confirmed, what changed. Every touched
   file's "Last confirmed" date is now today.

## Guardrails

- Five minutes. If the list is long, the rest waits for the next checkup.
- Never invent a belief to ask about — only what the files actually claim.
- Plain English, the owner's register. No file paths in the questions.
- Skip claims confirmed within the last 30 days unless something
  load-bearing visibly changed.
