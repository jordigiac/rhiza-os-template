# Correction ledger — patterns waiting for a second sighting

This system changes how it works on evidence, not on one bad moment
(contract law 11). This file is where the evidence waits.

**How it works:**

- The owner corrects something directly → it gets fixed today, and the file
  that caused it gets updated today. That skips this ledger entirely.
- The system notices something that *might* be a pattern → it lands here as a
  sighting. Nothing changes yet.
- The same thing happens again → it becomes a change, and the entry moves to
  APPLIED with a line saying what changed.
- A sighting sits for about 30 days with no second occurrence → the audit
  proposes retiring it. A pattern that never came back was noise.

| Date | What happened | Status | What changed |
|---|---|---|---|
| | | SIGHTING / APPLIED / RETIRED | |
