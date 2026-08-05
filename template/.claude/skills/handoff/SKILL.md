---
name: handoff
description: The save button. Closes a session so nothing gets lost - updates STATE.md, logs decisions with the why, parks loose ends, commits and pushes. Use when the owner runs /handoff, says they're done, wrapping up, or logging off.
---

# Handoff — close the session, lose nothing

The owner's one command. It must work every time and take under a minute.

## Steps

1. Look back over the session and collect four things: work that changed
   state, decisions the owner made, facts about the business that surfaced,
   and loose ends nobody resolved.
2. Update STATE.md:
   - Active rows that moved: update status, last updated, next step.
   - Finished work: move to Recently completed.
   - Do not touch "Up next" (that section changes only when builds are
     planned, never at save time).
3. For each decision the owner made, append to decisions.md: date, what was
   decided, and the why in the owner's own words. A decision is something the
   owner said yes or no to. If you are not sure something was decided, ask
   before writing it.
4. Add unresolved items to OPEN-QUESTIONS.md as dated one-liners.
5. The knowledge sweep: facts the owner stated directly this session get
   written into the right knowledge/ file now — dated, "Last confirmed"
   refreshed — and named in your close. Inferences get asked: filed on yes,
   parked or dropped on no.
6. Read back the open questions this session created — one line each — so
   the owner can answer any on the spot. Answered ones get filed and removed.
7. If this folder has a git remote: commit everything with a one-line plain
   English message (what happened, not file names) and push.
8. Tell the owner what was filed, in two or three plain lines. Done.

## Guardrails

- Never invent a decision, a status, or a date. Only file what happened.
- connections/, automations/, evals/, and audits/ never change during a
  handoff. knowledge/ changes only through the capture rules above — stated
  facts and approved asks, always dated, never silently.
- If the push fails, say so plainly and file everything locally anyway.
