# Document check — did the rewrite keep everything?

Runs on: any time this system rewrites, restructures, merges, or "tidies" an
existing file. When: every time, before saving.

Pass conditions — all must pass:

- **Nothing was dropped.** Every fact, name, number and caveat in the old
  version survives in the new one, or its removal was explicitly approved.
- **The meaning is unchanged.** Clearer wording is fine. A different claim is
  not.
- **The owner's load-bearing phrases are intact**, word for word.
- **It was read fresh from disk**, not from memory of reading it earlier in
  the session.
- **Every pointer still resolves.** If the file moved or was renamed,
  everything that points at it got fixed in the same pass.

Verdict: PASS or FAIL, plus a one-line critique.
