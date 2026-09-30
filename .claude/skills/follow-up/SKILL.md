---
name: follow-up
description: Drafts personal follow-up messages, one per person, in the owner's voice. Covers after a session, workshop or event (attended, no-show, bought, didn't buy), lead nudges from the pipeline's next actions, and payment reminders from the roster. Personal lines come only from what the owner noted; private notes shape the tone and are never quoted. Use when the owner asks to follow up with attendees, no-shows, leads or people who owe, asks for a payment reminder or "something for" a named person, "write my thank-yous", "who should I follow up with", or "who should I email after Saturday". Drafts only, in small batches; nothing is sent.
metadata:
  version: 2.0.0
  fitted-from: follow-up 1.2.0 (Jonathan's draft), fitted to the template 2026-09-29
---

# Follow-up — the right note to each person

After an event or a sales conversation, each person gets a message that
fits what actually happened with them, written the way the owner writes.
It's personal where the owner gave something personal, and clean and honest
everywhere else.

**Who owns what:** registrations owns who attended, paid or owes. leads owns
the pipeline, its stages and next actions. The program's file in
`knowledge/programs/` owns what was taught and the action step.
launch-facts and `knowledge/core/offers.md` own offer facts, prices and
links. messaging owns
launch-sequence emails (the calendar's rows). follow-up owns one-to-one
drafts only. It never changes a stage, a payment, attendance or a fact.

## Critical rules

1. **Personal only from the owner.** A personal line ("you mentioned
   wanting a side project") comes from the owner's notes, the leads entry,
   or what the owner says now. Never invent a moment, compliment, question
   or detail. Praise for how someone showed up ("you were so open in the
   room", "I noticed your courage") is a personal detail too, and needs an
   owner note that says it. People with no notes get the group version, and
   the reply says who they are, so the owner can add a line.
2. **Private notes stay private.** Notes like "cried in the hot seat", "money
   is tight", or "going through a divorce" guide the tone and what not to
   push. They are never quoted, hinted at or exposed, unless the owner
   explicitly okays using that detail. A hint includes any line about
   honesty, openness, courage, "showing up fully", a hard moment, or "I
   noticed" for someone whose private note is about that moment. Someone
   with a private note gets the same group thank-you as everyone else,
   written gently, with nothing that points at what happened. When in
   doubt, leave it out and flag it for the owner.
3. **The right message for each situation** (see the reference):
   attended, no-show, bought, didn't buy, unpaid or partly paid, refund
   requested, lead at each stage. Buyers and Won leads aren't pitched. The
   owner's standing rules still apply (a never-email segment, a no-pitch
   rule). When someone fits several, **priority decides**:
   1. a refund or customer issue
   2. a payment issue
   3. the post-event note
   4. a sales follow-up
   5. general nurture
   The highest one sets what the message must handle. A lower one can join
   only if it doesn't undercut it. A thank-you can carry a kind payment
   line. Nothing salesy goes to anyone with an open refund or payment issue.
4. **Held, not drafted, when a message shouldn't go yet.** Hold (no draft)
   and say why when:
   - the owner contacted them in the last few days (per the owner or the
     lead's last contact);
   - the person asked for space;
   - a follow-up is already planned for later;
   - a refund or customer issue is being handled;
   - the owner hasn't decided what happens next;
   - an opt-out or never-contact rule applies;
   - sources conflict in a way that changes what to say (rule 8).
   Held people are listed in the file and the reply, each with the reason.
5. **Facts exact, no pressure.** Links, prices, amounts owed, dates and
   deadlines are copied from the facts page, business profile, roster or leads
   entry. Missing is `[Calendar link needed]`, never a guess. A missing
   email address isn't a reason to hold: draft it and mark `[Email needed]`.
   Time since last contact is worked out from the dates, or left out
   (Sep 5 to Sep 28 is "a few weeks", not "a couple of weeks"). No invented
   urgency, scarcity, testimonials or results. A payment reminder states the
   amount and any due date the roster has, kindly, once. It never threatens.
6. **Voice first.** Write the write-like-me way: the owner's samples in
   `knowledge/core/voice-samples.md` first (their one-to-one messages
   above all), then `voice.md`. Before handing over, run the Gate
   (`evals/gate.md`), the voice check (`evals/standard/voice-check.md`),
   then the humanizer, which never overrides the voice. The owner's own
   laws about clients win (for example, a client email isn't ready until
   the owner has read it; nothing personal about a client goes in a file). Short, like a real one-to-one email.
   Use one clear next step when one actually exists. Never manufacture an
   ask just to make it actionable; a real thank-you can have none.
7. **Batches, approval and history.** Draft one situation group at a time
   (or up to ~8 people), then stop for the owner's review. Drafted →
   Approved (owner okays) → Sent (owner says it went). Drafted can be
   revised freely; Approved only before it's sent (it goes back to
   Drafted). **Sent is history**: never rewritten, even if the voice, offer
   or facts change later. A later correction is a dated *Update* under it. When the owner says a message was
   sent, remind them the pipeline or roster can be updated. That's done by
   leads or registrations, not here. Follow-up never edits those files.
8. **Conflicts are flagged, never settled quietly.** If sources disagree
   (the roster says paid, the owner says she still owes; the pipeline says
   Offer made, a note says she bought), trust the owning skill's record and
   newer confirmed information. Say what conflicts. If it changes what the
   message should say, hold that person until the owner settles it.

## Inputs

- The owner's request and any notes about people ("Priya asked about…").
- `registrations.md` for the event: attendance, payment status, amounts.
- `workspaces/pipeline/leads.md`: stages, next actions, notes.
- `knowledge/programs/<program>.md`: the lesson's action step, for
  after-session notes.
- `launch-facts.md` and `knowledge/core/offers.md`: offers, prices, links,
  replay details.
- `knowledge/core/voice-samples.md`, `knowledge/core/voice.md`: the voice.
- `knowledge/owner-profile.md` and `CONTRACT.md`: standing rules, including
  anything the owner said about clients.
- The pipeline, wherever it lives (see the leads skill): in a connected tool,
  or `workspaces/pipeline/leads.md`.
- `references/situations.md` (this skill's folder): what each situation's
  message does.

## Steps

1. **Find the people first.** Search the whole OS for each name the owner
   gave (the rosters in `workspaces/launches/`, the pipeline, the program
   files) before asking the owner anything. Never say you have nothing on
   someone until you've searched for their name.
   **Then find who and why.** After an event: everyone on the roster with
   attendance recorded (if attendance isn't recorded, ask for it; don't
   guess who came). Leads: open leads due today or overdue, or those the
   owner names. Also go through every open lead: one with no next action
   gets no draft but is named in the reply ("Joy has no next step; set one
   with your pipeline"). One whose booked call has already passed gets no
   draft either; ask whether it happened. Payments: Unpaid and Partial people.
2. **Sort people into situations** by the priority order (rule 3). Anyone
   who fits two gets the higher one, with the lower one carried only if it
   fits (an unpaid attendee: a thank-you with one kind payment line). Anyone
   who meets a hold reason (rule 4) is Held, not drafted.
3. **Draft**, one per person: a subject line, a short body in the owner's
   voice, the next step only if a real one exists (rule 6), exact links. A
   personal line only from the owner's notes (rule 1), with tone shaped by
   private notes (rule 2).
4. **Check before saving**, per person: the right person; the right
   situation and priority; no stale or conflicting fact; every personal
   detail traces to the owner; no private note leaks; links, prices and
   amounts match their source; no ask that isn't real; no standing rule
   broken; the tone fits; the status and history are right.
5. **Save** next to the source: `workspaces/launches/<launch>/follow-up.md`
   for a launch, its event, or a live call of the program it sold, and
   `workspaces/pipeline/follow-up.md` for lead nudges. One
   section per person, with an ID (F01…) that never changes.
6. **Reply.** Say "the drafts", label them DRAFT, and say where they live
   once, in plain words. Give:
   - the groups drafted;
   - this exact line, with names: "**No personal line yet:** Carla, Ana,
     Joy. Give me a detail for any of them and I'll work it in." Someone
     whose only note is private is on this list;
   - who is Held and why;
   - anything else held back (a private note, a standing rule, a missing link);
   - any conflict the owner needs to settle;
   - the next batch.
   Don't cite rule numbers or mention this skill, here or in the drafts'
   Based on notes. Say the
   reason in plain words.

## Held format

```markdown
## F06 — Beth Ortiz · Held
**Why:** refund requested; the owner hasn't decided (priority 1 issue open)
```

## Draft format

```markdown
## F03 — Carla Diaz · attended, bought · Second Act Saturday
**Status:** Drafted YYYY-MM-DD
**Subject:** …

[body]

**Based on:**
- Situation: attended, bought (registrations) · priority: post-event note
- Personal context: none given
- Tone only (private): owner note to be gentle, never mentioned
- Unknown, not assumed: whether she booked a coffee chat yet
**Placeholders:** none / [list]
```

## Needs the owner's yes

- Approving and sending every message.
- Using a private detail in a message (only if the owner says to).

## Guardrails

- Don't change stages, payments or attendance. Tell the owner which skill
  records the outcome.
- Don't write launch-sequence emails; those belong to messaging and the
  launch calendar.
- Don't email people outside the owner's relationship (no cold outreach
  to scraped contacts).
