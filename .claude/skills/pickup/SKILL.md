---
name: pickup
description: The session opener. Reads the board, the open questions, the journal and what's happened in git, then briefs the owner on where things stand and what's next. Changes nothing. Use when the owner says hey, I'm back, where were we, what's going on, or runs /pickup.
---

# Pickup — where were we?

Read-only. **A pickup that edits a file has failed.** It orients, it never
files. The owner has been away; this is the two minutes that put them back in
the chair.

## Steps

1. **Read, fresh from disk:** STATE.md (what's alive, and anything marked as
   the current focus), OPEN-QUESTIONS.md, the top entry of journal.md, and the
   last few entries in decisions.md if the board points at a why.
2. **Check git, and only report it.** Has anything changed since the last
   close? Is anything uncommitted or unpushed? Say it in one line and suggest
   the handoff if there's work sitting unsaved. Never sync, never commit.
3. **Brief them in under ten lines:**
   - What closed last time.
   - What's alive now.
   - What's waiting on them, if anything.
   - One suggested next move — proposed, never decided.
4. **Anything that moved while they were gone** gets one line each. Nothing
   moved is also an answer; say that in one line and move on.
5. **Then stop and let them talk.** If they state facts or answer questions
   during the pickup, the normal rules take over from there: file what they
   state, dated, out loud.

## Guardrails

- Read-only. No files change, including STATE.md.
- Ten lines or fewer. Orientation, not a report.
- No guilt about a gap. Two days or two months, the tone is the same.
- If getting oriented takes more than about three minutes of reading, the
  last handoff was thin. Say so, once, so the next one is better.
