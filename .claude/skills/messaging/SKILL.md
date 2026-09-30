---
name: messaging
description: Writes the copy for a launch's planned sends, in the owner's own voice. Covers emails, social posts, and partner swipe copy, drafted in small batches of 3–5 related sends against the IDs in the launch calendar. Every link, date, time, price and deadline is copied from the launch facts page, never retyped or invented. Use when the owner asks to write, draft, or redo launch emails, posts, invites, reminders, cart-open or closing emails, or partner swipe copy, or says "write the next batch". Also use when a facts page change sends drafts back for rewriting. Reads facts from launch-facts and the plan from launch-calendar; jv-kit packages the partner copy for sending.
metadata:
  version: 2.0.0
  fitted-from: messaging 1.2.0 (Jonathan's draft), fitted to the template 2026-09-29
---

# Messaging — the words for each planned send

The calendar says which send goes when, to whom, and with which link. This
skill writes what it says: subject line and body for each email, the caption
for each post, and the swipe copy partners send to their own lists. It
writes in batches so the owner can correct the voice early.

**Who owns what:** launch-facts owns the facts. launch-calendar owns the plan
(dates, audiences, IDs). messaging owns the copy only. It never changes a
date, audience, link or calendar row, and keeps no facts of its own: the
drafts file holds copy, not a second copy of the facts page. jv-kit packages
partner copy for sending. Sales and landing pages aren't this skill's job;
if the owner asks for one, write-like-me drafts it from the same facts
page.

## Critical rules

1. **Facts come from the facts page, word for word.** If the facts page
   says TBD for something your offers file has a usual value for (the
   session time, the room), the facts page wins: use a placeholder and ask
   whether the usual value holds this time. Every link, date, time,
   price, deadline, bonus and event name is copied from the facts page. Never
   retype a link from memory or from another draft. A fact the facts page has as
   TBD becomes a plain, visible placeholder in the copy: `[Replay link
   needed]`. Placeholders are always in square brackets and end in "needed",
   so the owner (and anyone searching the file) can spot every gap before
   anything is loaded.
2. **The row decides, the copy follows.** Date, audience, purpose and link
   come from the calendar row. If a row is contradictory or clearly wrong
   (a pitch to buyers, an invite to registrants, a link that isn't on the
   facts page), don't draft it and don't edit the calendar. In the reply, say
   which row, what conflicts, why copy can't safely be written, and the fix
   ("Ask the calendar to change E09's audience to non-registrants, then I'll
   draft it"). If the owner gives a new launch fact, it goes through
   launch-facts first, then the calendar, then the copy.
3. **No invented proof or pressure.** Testimonials, client results, numbers,
   "spots left", and deadlines appear only if they're in the facts page or a
   knowledge/ file, in the owner's words or with their approval. Otherwise
   use a placeholder: `[Testimonial needed: a real client, and what changed
   for them]`.
   The owner's own story (age, years in a job, clients served, what
   happened to them) appears only as a knowledge/ file states it: never
   rounded ("19 years" stays 19), never added to. Event details (length,
   format, what's covered) come only from the facts page. **The same goes
   for the offer itself:** what buyers get, the promise, how it runs, how
   big the group is ("small cohort", "you'll leave with a plan", "bring a
   real problem each week") appear only as the facts page or
   `core/offers.md` states them. If the owner's promise isn't captured,
   use a placeholder: `[What they'll walk away with, in your words,
   needed]`, and ask for it in the reply.
   Scarcity only when the facts page has a real seat cap or deadline. Unusual
   results ("doubled her income") need the owner's note on typical results.
   Made-up endorsements and false urgency can break advertising rules. This
   OS doesn't write them.
4. **Partner copy discloses the partnership.** Swipe copy for JV partners
   includes a plain line that they earn a commission (or, for a swap with
   no commission, a plain line that it's a friend's program they're
   sharing). Where the partner signs or adds their own touch, write
   `[your name]` / `[your story]`, with `[your name]` only at the
   sign-off. Those are fill-ins for the partner, not gaps, so they don't
   end in "needed".
   **Swipe copy is what the partner sends to their own list,** written for
   the partner's send rows in the calendar (the rows where the partner
   mails), never for the kit-due or reminder rows. When the owner asks for
   "Priya's email" or "Dana's swipes", that means the partner's send rows.
   A private note from the owner to the partner is not swipe copy; jv-kit
   writes that as the cover note.
   **Swipe copy never speaks for the partner's readers or borrows the
   owner's.** No claims about how the partner's list reacted ("a couple of
   you replied", "you've been asking me"), and the owner's client quotes
   never appear as things the partner heard. Anything personal is a
   `[your story]` fill-in.
5. **Batches, not the whole launch.** Draft 3–5 related sends at a time, in
   calendar order. **At least three**, crossing a phase if needed (the
   last invite and the cart-open email can share a batch). Fewer only when
   fewer Planned rows are left, and say so: draft → owner reviews → revise → owner approves → next
   batch. The first batch is the voice check, so wait for the owner's
   reaction before going on. Never write the entire sequence in one go,
   even if asked. Offer the next batch.
6. **Drafted is not approved.** Copy is ready to load only when the owner
   explicitly approves it. Statuses: Drafted (by AI) → Approved (by the
   owner) → Loaded → Sent. Only the owner or team marks Loaded or Sent.
7. **History is kept.** Loaded and Sent copy is never rewritten as if it
   had always been right (see *When the facts page changes*).
8. **Voice beats the humanizer.** The owner's voice comes first. The
   humanizer is a final check that removes obvious AI patterns. It may not
   change the owner's tone, words, rhythm, claims, structure or intent. If
   the two conflict, the owner's voice wins.

## Inputs

- `workspaces/launches/<launch>/launch-facts.md`: the facts. Note its status.
- `workspaces/launches/<launch>/calendar.md`: the rows (ID, date, time,
  To, Exclude, purpose, link, status).
- `knowledge/core/voice-samples.md`: real things the owner wrote. The
  evidence, read first.
- `knowledge/core/voice.md`: the owner's voice described, plus any rules
  they stated.
- `knowledge/core/offers.md` and `knowledge/core/audience.md`: the offer,
  who it serves, and the phrases those people actually use.
- `references/send-types.md` (this skill's folder): what each kind of send
  is for, how long, and what it asks. Read the entries for this batch.
- `workspaces/launches/<launch>/messaging.md`, if it exists: earlier
  drafts and the owner's feedback.
- The write-like-me skill (`.claude/skills/write-like-me/SKILL.md`): how
  this OS writes as the owner. Messaging follows it for every draft.
- The quality check: `evals/gate.md` and `evals/standard/voice-check.md`,
  then the humanizer skill (rule 8).

## Steps

1. **Find the launch and the batch.** Read the facts page and calendar. If the
   calendar doesn't exist, say so and stop: the calendar comes first. If
   the owner okays the plan in the same message ("plan's approved"), set
   the calendar's status line to `Approved, YYYY-MM-DD` first, the way
   launch-calendar does, but only if the facts page is Confirmed.
   Otherwise say the facts page needs confirming first, and draft anyway. The
   batch is the next 3–5 Planned rows in date order that belong together
   (the invites, one event day, the cart-open pair, the close sequence),
   unless the owner named rows. Skip automation rows only if their copy is
   already in the email tool.
2. **Read the voice, the write-like-me way.** Samples first: load the
   three to five in `voice-samples.md` closest in format to this batch (an
   email for an email, a post for a post). Then `voice.md` for the
   distilled rules. When the samples and the description disagree, the
   samples win, and say so in the reply so the description gets fixed.
   Look for patterns, not phrases: tone, sentence rhythm, vocabulary, paragraph length, how direct
   they are, how they tell stories, humor, emotional intensity, how they
   teach, how they sell, how they ask for the click, and habits that repeat
   (a greeting or sign-off they use every time is a habit to keep).
   Samples are evidence, not a script. Don't reuse a distinctive line just
   because it's in a sample. Explicit voice rules the owner stated ("never
   say hustle") are hard rules.
   **Judge coverage:** do the samples show this kind of writing? Two
   newsletters say little about a closing-day sales email or an Instagram
   caption. If coverage is thin, or there are no samples, draft anyway from
   what's there and the offers and audience files, and note in the reply that voice
   confidence is limited and which kind of example would help most.
3. **Draft each send** from its row and the send-types reference:
   - **Email:** subject line (plus one alternative), preview text, body,
     one clear ask, the row's link by exact facts page value, sign-off as in the
     samples.
   - **Post:** caption for the channel on the row, one ask. No links in the
     caption if the channel doesn't allow them; say "link in bio".
   - **Partner swipe:** written for the partner's list, in a neutral voice
     the partner can adapt, with `[your name]` fill-ins, their tracking link from
     the facts page, and the commission disclosure.
   Write to the row's audience. A registrant is already in, so don't invite
   them. A non-buyer after cart open is being sold to, with care.
4. **Check every draft before saving.** Read each one against the facts page:
   - Every link in the body is the facts page's actual URL, character for
     character. Never a stand-in like `[registration link]`. Brackets are
     only for facts the facts page has as TBD.
   - Voice matches the patterns from step 2, and any greeting or sign-off
     the samples use consistently is kept.
   - Every date, weekday, time and time zone matches the facts page and calendar.
   - Every price, deadline and bonus matches the facts page, including the
     wording around it: a deadline that runs *through* Dec 3 is never
     "before Dec 3". If the facts page has no time for a deadline, the
     copy says the date only, or `[Early-bird end time needed]`.
   - Nothing states a fact the facts page doesn't have, and no testimonial,
     result or scarcity was invented. Check subject lines and preview text
     too: "registration closes tonight", "only a few seats" and "last
     chance" count as facts, and need a deadline or cap in the facts page.
   - No sentence is copied or nearly copied from a voice sample. Compare
     each subject line and opening against the samples; reword any echo.
     When a sample is the same kind of email for the same offer (last
     year's launch email for this program), use it for rhythm and length
     only: the structure, the angle and every line must be new.
   - Every number and personal detail in the copy (an age, "19 years",
     "12 minutes", "3 mornings") points to a line in the facts page or a
     knowledge/ file. If you can't point to it, cut it or make it a placeholder.
   - Every claim about the offer (what it is, how it runs, its size, what
     buyers get) points to a line on the facts page or in `core/offers.md`.
     Read each draft sentence by sentence for this; it's the claim that
     slips in most.
   - The quality check, in this order: the Gate (`evals/gate.md`), then the
     voice check (`evals/standard/voice-check.md`), then the humanizer
     pass, under rule 8. Re-check the voice after the humanizer. The
     Gate's facts line is met when every price, date and link traces to
     the launch facts page or `knowledge/core/`.
   Fix, then check again. Two tries with no real improvement means stop
   and say what's stuck.
5. **Save** into `messaging.md` in the launch folder, one section per row,
   headed with its ID: `## E03 — Invite 2 · Sun Nov 8, 8:00am MT · to
   non-registrants (excl. past-pivot-lab)`. Copy the row's date and audience
   into the heading exactly; don't recompute them. Keep earlier sections.
6. **Mark progress.** In the calendar, change only the Status cell of each
   drafted row from Planned to Drafted. Touch nothing else in the calendar.
   Status is the one field messaging may write there.
7. **Reply briefly:** which rows you drafted (ID + purpose), placeholders
   that need the owner (TBD links, testimonials), anything you flagged.
   Name any blocked rows (rule 2). **Always** end with one voice line from
   the coverage check in step 2, even when coverage is good ("Voice: solid,
   I had two of your launch emails to go on."). When it's thin: "Voice
   confidence is limited. I only have your newsletters to go on. A past
   sales email would help most." Say "the drafts" or "the facts page", and
   say where the drafts live once, in plain words ("they're in the launch
   folder, next to the calendar"). Label them DRAFT. Then ask for their
   reaction or approval, and name the next batch: "Next up: E06–E08, Day 1 of Pivot
   Week. Want me to go on?"
8. **On the owner's approval** ("these are good", "approved"), set those
   rows' Status to Approved in both places: the draft's section here, with
   the date, and the row's Status cell in the calendar. Approval covers
   only the rows the owner approved.

## Feedback

- **Edits to a draft** fix that draft. They don't become a rule.
- **When the owner rewrites a draft themselves,** ask once: "Want me to add
  your version to your voice samples?" On a yes, both versions go into the
  Rewrites section of `knowledge/core/voice-samples.md` with one line on
  what changed. Their edit teaches the voice more than anything else.
- **A stated preference** ("I never open with a question", "always sign off
  'Talk soon'") is a voice rule. File it in `knowledge/core/voice.md` under
  *Rules the owner stated*, dated, in the owner's exact words, so it's
  clearly theirs and not an AI guess. It's the owner saying it, so it's
  their word (contract law 9). Say you did. Future batches follow it.
- **The same correction twice** without a stated rule: ask whether it
  should become a rule. File it only on yes.
- Never infer a permanent preference from a single edit.
- After feedback, revise the batch. Revised copy goes back to Drafted until
  the owner approves it.

## When the facts page changes

The calendar handles dates. When rows come back to Planned, or the owner
says a fact changed:

1. Find every draft that uses the old value (link, date, price, deadline).
2. **Drafted or Approved rows** (not yet loaded): rewrite only those sends,
   keep their IDs, set them to Drafted (approval is needed again), and list
   what changed.
3. **Loaded or Sent rows:** never overwrite the copy. Keep it, and add a
   correction block under it:

   ```markdown
   **Correction needed (YYYY-MM-DD)**
   - Issue: the registration link changed (…/pivot-week → …/pivot-week-2)
   - Replacement: [the corrected copy, for a Loaded row]
   - Action: edit this email in your email tool before it sends Mon Oct 26
   ```

   A Sent email can't be fixed; its original stays as the record of what
   went out. If a follow-up is needed, the calendar adds a correction row,
   and messaging drafts that row. The row's status never changes here. Put
   these first in the reply, with dates.

## Draft format (messaging.md)

```markdown
# Messaging — [Launch name]

*Built from the facts page's YYYY-MM-DD version and the calendar's YYYY-MM-DD version.*

## E03 — Invite 2 · Sun Nov 8, 8:00am MT · to non-registrants (excl. past-pivot-lab)
**Subject:** … · **Alt subject:** … · **Preview:** …

[body]

**Link used:** Registration page → [exact facts page value]
**Placeholders:** none / [list]
**Status:** Drafted YYYY-MM-DD (or Approved by owner YYYY-MM-DD)
```

## Needs the owner's yes

- Approving any draft. Copy is ready to load only after that.
- A testimonial, result, or number that isn't already in the files.
- Turning a repeated correction into a voice rule.

## Guardrails

- Plain English in the reply. Say where the drafts live once, in plain
  words.
- Nothing is sent, loaded or scheduled. Drafts only (contract law 4).
- Don't write copy for rows that aren't in the calendar. If the owner asks
  for an extra email, the calendar adds the row first.
- Don't write sales pages or landing pages here. write-like-me does those.
