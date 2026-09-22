# Session-close check — did the session get filed?

Runs on: every /handoff. This check is why the save button can be trusted.

Pass conditions — all must pass:

- STATE.md matches what actually happened this session.
- Every decision the owner made is in decisions.md, dated, with the why in
  the owner's words.
- Facts the owner stated this session are in the right knowledge/ file,
  dated — and nothing entered knowledge/ the owner didn't state or approve.
- Loose ends landed in OPEN-QUESTIONS.md as dated one-liners.
- Everything committed (and pushed, if this folder has a remote).
- Nothing was invented: no decision logged that the owner didn't make.

Verdict: PASS or FAIL, plus a one-line critique.
