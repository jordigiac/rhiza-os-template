# evals/ — how quality works in this OS

**The one rule: before anything goes out on the owner's behalf, it gets
checked.** The Gate runs on everything. Then one routed check runs, depending
on what the work is. Then the humanizer. Then it lands as a draft for the
owner's yes.

This is not a button the owner presses. It is how every skill in this system
ends.

## The Gate — always

`gate.md`. Three parts: the words check (nothing sent, no AI tells, facts
traced to core), done-the-way-the-owner-thinks (simple first, their call,
verified not plausible, manual first, worth their review time), and the
handoff shape (what was done, what needs their eyes, open questions, and what
wants to go into the knowledge base on their yes).

## Then the one that fits the work

| The work | The check |
|---|---|
| Anything a person will read — emails, posts, copy, messages | `standard/voice-check.md` |
| Any statement about this business — a price, a date, a name | `standard/truth-check.md` |
| Rewriting or restructuring a file that already existed | `standard/document-check.md` |
| A conversation where a decision got made | `standard/consult-check.md` |
| Going and finding something out about the outside world | `standard/research-check.md` |
| Closing a session | `standard/session-close-check.md` |

Verdicts are **pass or fail plus a short critique**, never a score out of
ten. A critique holds the nuance; the verdict holds the line.

## The other two layers

**Custom exams.** Every automation and custom skill gets its own folder here,
copied from `_template/`: a dataset of test cases, scorers that define what
done looks like, and dated scorecards. They are the graduation exams of the
trust ladder in `automations/`. Nothing moves from beta to automated without
passing its exam consistently.

**The audit** is the eval of the system itself. Monthly, read-only, reports
into `audits/`.

## The correction ledger

`correction-ledger.md` is where a possible pattern waits for a second
sighting before this system changes how it works. The owner's direct
corrections skip the wait and get fixed the same day.

## Grading your own work

Two honest limits, worth knowing:

- **A system checking its own draft is a generous grader.** Where the tools
  allow it, have a fresh read do the checking, with no memory of writing the
  thing. "I couldn't verify this" never quietly becomes "pass."
- **Two attempts with no real improvement means stop.** Say what's stuck and
  hand it over with the problem named.

The owner benefits from this folder without ever touching it, and owns it:
the datasets and scorecards are this business's records, and they stay here.
