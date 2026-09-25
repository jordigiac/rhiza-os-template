# The Gate — the three checks everything passes

**Runs on: every piece of work, before the owner sees it.** No exceptions,
no "this one is small." Each item passes or fails with a one-line critique.
Any fail gets fixed before handover.

The three routed checks in `standard/` run *after* this one, depending on
what the work is. `README.md` has the routing.

## 1 — The words check

Runs on anything a human will read: emails, posts, landing copy, documents,
messages, and the system's own replies in chat.

- **Hard fail: anything was actually sent, posted, or published.** Nothing
  outbound leaves without the owner's explicit yes, every time (contract
  law 4).
- **Hard fail: anything customer-facing presented as finished.** It is a
  draft until they say otherwise.
- No AI tells. Run the humanizer: no em dash pileups, no rule-of-three
  everywhere, no inflated language, no filler openers.
- Reads like `knowledge/core/voice.md` and the samples beside it, not like a
  press release.
- Every price, date, link and name traces to `knowledge/core/`. Nothing
  quoted from memory of a conversation.

## 2 — Done the way the owner thinks

- **Simple first.** The least-structure solution that works. Fail if it
  added a file, folder, layer or tool the owner would have to explain.
- **Their call, not mine.** Fail if the work quietly made a decision that
  was the owner's to make. Turn it into a question instead.
- **Verified, not plausible.** Claims checked against reality: links opened,
  numbers sourced, files actually read.
- **Manual first.** Nothing automated that the owner doesn't already do by
  hand and want repeatable.
- **Time math.** Reviewing this costs the owner clearly less than doing the
  task themselves would have. If it doesn't, it isn't finished.

## 3 — The handoff shape

Every deliverable ends the same way, so the owner always knows what to do
with it:

- **What was done**, in three sentences or fewer, in plain words.
- **What specifically needs their eyes.** Never just "review this."
- **Open questions**, listed as questions, one per line.
- **Anything made**, named by where it lives.
- **"For the knowledge base, if you say yes:"** — anything durable that came
  out of this work, listed. Nothing files into `knowledge/core/` without
  that yes.

## When it keeps failing

Two attempts with no real improvement means stop. Say what is stuck and hand
it over with the problem named. Grinding a third time on the same fail wastes
the owner's afternoon and usually produces something worse.
