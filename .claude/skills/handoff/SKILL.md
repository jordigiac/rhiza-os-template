---
name: handoff
description: The save button. Closes a session so nothing gets lost - files what the owner said, logs decisions with the why, updates the board, takes their note for the journal, then commits and pushes safely. Use when the owner runs /handoff, says they're done, wrapping up, logging off, or that's it for today.
---

# Handoff — close the session, lose nothing

The owner's one command. It must work every time and take under a minute.

**Run it, don't offer it.** When the owner signals they're done, this runs and
then reports. The hourly backup underneath it saves files; only this files
facts.

## Hard rules, read first

- **Never invent** a decision, a status, a date, or a fact. Only file what
  actually happened.
- **Commit before you pull.** Nothing local can be lost to what comes down.
- **On a merge conflict: stop.** Name the files that disagree and wait for the
  owner. Never force, never discard one side to make it go away.
- **Never rewrite history.** No force-push, no amending what's already pushed.
  This repo is the undo path.
- **Never commit a secret.** Before staging: confirm `.env` is ignored and
  untracked, and scan what's staged for keys, tokens and passwords. Anything
  that looks like a credential stops the commit cold and gets said out loud.
- connections/, automations/, evals/ and audits/ don't change during a
  handoff. `knowledge/core/` doesn't either, unless the owner said so in this
  session (contract law 9).

## Steps

1. **Look back over the session** and collect five things: work that changed
   state, decisions the owner made, facts about the business that surfaced,
   loose ends nobody resolved, and corrections the owner gave.

2. **Update STATE.md.** Rows that moved get their status, date and next step
   updated. Finished work moves to Recently completed. Don't touch "Up next",
   because that section changes when builds get planned, never at save time.

   The board's rules, every time:
   - **Never delete a thread.** Finished and dropped ones get marked and
     dated, and leave the board only when the owner confirms.
   - **Never invent a thread.** Rows come from what the owner said.
   - **Every state is a proposal.** They correct any line by saying so.
   - **One line per thread.** The next-step cell answers what happens next and
     what's holding it, in fifty words or fewer. History belongs in
     decisions.md and journal.md, not on the board.

3. **Log the decisions.** For each one, append to decisions.md: the date, what
   was decided, and the why in the owner's own words. A decision is something
   they said yes or no to. If you're not sure something was decided, ask
   before writing it.

4. **File the facts — the knowledge sweep.** Facts the owner stated directly
   go into the right knowledge/ file now, dated, "Last confirmed" refreshed,
   and named out loud in your close. Inferences get asked: filed on yes,
   parked or dropped on no. Anything that belongs in `knowledge/core/` gets
   *proposed*, never written silently.

   Themes too: a preference the owner repeated this session is worth naming.
   Ask what's going on, then propose the line for PERSONA.md, decisions.md, or
   the contract. Their yes writes it.

5. **Sweep the corrections.** Anything the owner corrected this session
   updates the file that caused it, so it can't recur. If it's a first
   sighting of a pattern rather than a direct correction, note it in
   `evals/correction-ledger.md` and leave it to wait for a second.

6. **Take the journal note.** Ask if they want to leave a note for tomorrow.
   Whatever they say goes into journal.md at the top, dated, structured into
   its essence: their meaning kept exactly, the wording tidied only as far as
   PERSONA.md says they like. No note is a fine answer; skip it and move on.

7. **The open-questions pass.** Read back the questions this session created,
   one line each, so they can answer on the spot. Then scan the rest of the
   file and surface any that today's work just answered. Answered ones get
   filed into decisions.md and struck from the list.

8. **The close check.** Ask yourself: does anything durable live only in this
   chat? A decision not logged, a fact not filed, a loose end on no board, a
   correction not yet taught. If yes, do it now. Say in one line what this
   check caught, or that it caught nothing.

9. **Save it.** In this order:
   - Fetch and look. Uncommitted work, ahead, behind: those three facts decide
     the rest. Nothing to do is a valid answer; say it in one line and stop.
   - Run the secret check above.
   - Commit everything with a plain-English message: what happened and why it
     mattered, readable in six months. Never "update", never a bare date.
   - Pull with rebase if behind, so the owner's work lands on top. A conflict
     means stop.
   - Push, then read the remote back to confirm it landed. A push that printed
     no error still gets verified.
   - If the folder is synced by OneDrive, iCloud or Dropbox, a locked file can
     make git fail. Say so, wait a moment, try once more, then report honestly.
   - If this surface can't run git at all, say so plainly, confirm the files
     are saved on disk, and note that the hourly backup will version them. The
     save never silently pretends.

10. **Report in two or three plain lines:** what got filed, what the close
    check caught, and the commit that's now on GitHub. **If anything failed,
    that's the first line.** A silent failed push is worse than no save,
    because it leaves them believing they're backed up.
