---
name: launch-facts
description: Creates and keeps the launch facts page, the one page that holds a launch's offer, event, dates, prices, audience, partners and links. Every other launch skill builds from it. Use whenever the owner mentions a new launch or promotion (webinar, challenge, masterclass, workshop, course, program, cart open or close, partners promoting it), a launch they're already in the middle of, whenever a launch link, date, price or partner changes ("the link changed", "we moved the date"), and whenever the owner answers a launch's open questions, tells you how their email list is split, or says the launch facts are right ("that's everything", "confirm it"). Use it immediately, even when details are missing or contradictory. It saves what's known and flags the rest. For the dated plan, see launch-calendar; for the emails, see messaging.
metadata:
  version: 2.0.0
  fitted-from: launch-brief 1.3.0 (Jonathan's draft), fitted to the template 2026-09-29
---

# Launch facts — the one page every other launch step reads from

The launch facts page is where a launch's facts live. The calendar, the
emails, the posts and the partner kits all read from it and never retype a
link or a date. When a fact changes, it changes here first. Wrong links and
wrong rooms happen when facts live in five places.

## Who owns what

- **launch-facts owns the launch's facts.** Offer, prices, dates, times,
  links, audience, partners and terms are written only here.
- **launch-calendar owns the dated plan. messaging owns the copy.** They
  read facts from this page and never decide or overwrite one.
- **Standing facts live in `knowledge/core/`.** What an offer is and its
  list price live in `core/offers.md`. This page holds what's true for this
  one launch.
- When the owner gives a launch fact during any other task, it gets filed
  here first, the same way as below, and then the other task goes on.
  Another skill never edits this page directly.

## Draft and Confirmed

- **Draft:** everything captured so far. Gaps and clashes are fine. Write
  the Draft anyway. Other skills may plan from a Draft but must show that
  it's a Draft.
- **Confirmed:** only when the owner says the page is right *and* no
  clashes are open. If they say yes while a clash is open, settle the clash
  first. Remaining TBDs stay TBD and stay listed.
- Never mark it Confirmed on your own, and never treat a Draft as
  Confirmed.

## Critical rules

1. **Never invent.** Every link, date, time, price, commission, email
   group, name and email address comes from the owner's words or a
   knowledge/ file. Anything else is `TBD`. No placeholder URLs, no guessed
   values. A hedged fact from the owner ("probably the 9th") is kept, marked
   unconfirmed (step 2).
2. **Defaults are shown, not applied.** Standing facts from knowledge/ (what
   the offer is, its list price) may be filed, marked
   `(from your offers file)` and read back to the owner. Per-launch choices
   that usually repeat (the partner rate, the Zoom room, a send time) are
   written `TBD (usual: …)` until the owner confirms them for this launch.
3. **Flag every clash. Resolve none.** If two facts disagree (the owner
   vs. the real calendar, the owner vs. a knowledge/ file, one message vs.
   an earlier one), write both sides with where each came from, and ask.
   Never pick one. Clashes and gaps never stop the page: write it as a
   Draft anyway, then raise every clash in the same reply, not one at a
   time.
4. **Every time gets a time zone; every date gets its weekday**, checked
   against a real calendar for every date the owner gives. Use whatever
   calendar tool you have (for example `date -d 2026-11-12 +%A` in a
   terminal). If you have none, work it out carefully and check it twice.
   A weekday the owner said that doesn't match is a clash. A date with no
   year means its next occurrence after today. "My time" means the owner's
   time zone from `knowledge/core/business-profile.md`. "Midnight" on a
   date is written `11:59pm` that date, marked `(confirm: end of day?)`,
   and asked about, since it can mean the start of the day.
5. **Past dates.** For a new launch, a key date already in the past is a
   clash. For a launch the owner says is already running, dates already
   passed are history, not clashes: file them as given.
6. **Facts only.** Don't draft emails, posts, pages or partner notes. Those
   are later skills. Don't write launch facts into decisions.md or
   knowledge/.
7. **Standing facts go to their one home, now.** When the owner states a
   fact that isn't about this one launch (how their email list is split,
   their time zone), file it where it lives in `knowledge/core/`, in their
   words, dated, and say so in one line. "In their words" means their
   sentence as they said it, quoted; if the owner asked for their words
   kept exactly (see `knowledge/owner-profile.md`), never reorder,
   bullet or gloss it. They just said it, so it is their word under
   contract law 9. Don't ask permission to file what they just
   told you, and never file it only inside the launch folder or a
   connection file. The launch page then points at it.
8. **The owner's standing rules win.** Check the "never do" lines in
   `knowledge/owner-profile.md`, and any law the owner added to
   `CONTRACT.md`, against the audience. If one applies, raise it as a
   question, even when the owner asked for it this time.

## Inputs

- The owner's message: whatever they gave, in any order.
- `knowledge/core/offers.md`: the offers, list prices, sales links.
- `knowledge/core/audience.md`, the *Your email list* section: how the
  owner splits their list, and who never gets a sales email.
- `knowledge/core/business-profile.md`: the time zone.
- `knowledge/core/team-and-tools.md`: who's on the team.
- `knowledge/owner-profile.md` and `CONTRACT.md`: the "never do" lines.
- `knowledge/partners/`: each partner's history and usual terms.
- `workspaces/launches/`: existing launches (is this one new?).
- `workspaces/_template/launch-facts.md`: the blank page to copy.

## The email list, asked once

The page needs to know who gets the emails. Check `core/audience.md` for a
*Your email list* section.

- **If it's there,** map the owner's words to those groups. "Everyone" or
  "the whole list" gets written out as the actual groups, marked
  `(confirm)`.
- **If it isn't,** ask once, in plain words: "How do you split your email
  list? For example: newsletter, past buyers, people who took a free
  quiz. And is there anyone who should never get a sales email?"
- **When they answer,** fill the *Your email list* section of
  `core/audience.md` (add the heading if it isn't there) with their answer,
  in their words, dated, and say so in one line. No second permission
  question: they just said it (rule 7). Every skill reads it from there,
  and nobody asks again.
- If the owner doesn't know or skips it, the page says `Send to: TBD` and
  the launch goes on.

## New launch

1. **Know today's date** (from the session, or a tool like `date +%F`).
   Then, **new or existing?** Look in `workspaces/launches/`. If a folder
   already covers this offer and date, the owner is updating it: answers to
   open questions go to step 9, and changed facts go to *Changing a
   launch*.
   **An older page in the folder.** If that folder holds a page from before
   this skill (a `RUN.md` or `CONTEXT.md`), it becomes the launch facts
   page: carry every fact on it into `launch-facts.md`, in the new
   sections, then add today's new facts on top. Every link, channel,
   person and open question on the old page comes across; open questions
   go under *Still TBD*. Before you reply, read the old page line by line
   against the new one and carry anything missing. Then, in the reply
   itself, ask: "Your old launch page is still in the folder. Want me to
   box it into your archive so there's only one?" Never delete it, and
   never promise the offer on the page without making it in the reply.
2. **Pull out the facts** into the page's fields. Map vague words to real
   things only when the match is near-certain, and mark the match
   `(confirm)`: "the quiz people" → `quiz-takers (confirm)`. A hedged fact
   ("probably the 9th", "I think $997") is written with
   `(unconfirmed: you said "probably")` and goes in the questions. Offer
   details and list prices follow rule 2. Email groups follow *The email
   list, asked once*. Otherwise, TBD.
3. **Run the checks** and list every problem under *Clashes*. A clash
   names both sides and where each came from ("you said Tuesday; Nov 12 is
   a Thursday"). If you can't point to both sides, it isn't a clash.
   - Weekday matches the date. Every time has a zone.
   - Order holds: promotion starts → event → cart opens → cart closes.
     Early bird and every bonus deadline fall inside the cart window. Early
     bird costs less than full price.
   - Each partner's send window ends before the event (or before cart
     close when there's no event). Each partner has a contact, a
     commission, and a tracking link (or TBD).
   - Email groups exist in the *Your email list* section. Excluded groups
     stated.
   - Price matches `core/offers.md`, or the change is noted.
   - Program sessions, if given: each has a zone, and the first falls on
     or after cart opens.
4. **Name the folder** `workspaces/launches/<offer>-<month>-<year>/`, plain
   words, lowercase, hyphens, dated by the event (or by cart open when
   there's no event). Example: `pivot-lab-november-2026`. If the owner names
   a round ("January round"), use it (`pivot-lab-january-2027`). Never reuse
   a folder that already exists. Copy `workspaces/_template/launch-facts.md`
   into it as `launch-facts.md` and fill it in. Status: Draft. If the blank
   page is missing, say so and build the same sections from memory of this
   skill.
5. **Check the page before you reply.** Re-read it line by line:
   - Every date is after today, with the right year (rule 5 covers a launch
     already running).
   - Every weekday you wrote, including partner windows, matches its date.
     Check each one with your calendar tool if you have one.
   - Every time is one the owner gave. No time you weren't given; that's
     TBD.
   - A clashing field shows the owner's words plus "see Clashes". It never
     shows a value you picked.
   - Each partner window was compared to cart close (or the event).
   - Every price, date and link traces to the owner's words or a
     knowledge/ file (the truth check in `evals/standard/truth-check.md`).
   Fix anything that fails, then check again.
6. **Add one row to STATE.md → Active:** the launch name, `LIVE`, today's
   date, and the next step ("settle the open questions, then the
   calendar").
7. **Reply to the owner, short.** Open with one line like "Launch facts
   drafted for Pivot Lab, November. It's in your launches folder, under
   `pivot-lab-november-2026`." Then:
   - A 3–5 line read-back: offer, event, cart dates, audience, partners.
     Repeat the owner's facts as given. Where a fact clashes, say "see
     below". Never smooth it over. Every time in the read-back carries its
     zone, and a zone that isn't confirmed says so ("midnight, Eastern, if
     that's your zone").
   - Clashes, one line each, with the question to settle it.
   - Up to 5 questions for the most important TBDs. Links and times first.
     The rest stay TBD on the page.
   - **Settled elsewhere.** Before replying, search the OS for anything
     today's facts answer or make wrong: a "year not confirmed" note in
     `core/offers.md`, a line in `OPEN-QUESTIONS.md`, an old date on the
     board. Standing facts in core get filed per rule 7 and said. Every
     other hit gets one line in the reply with an offer to update it.
     Never leave another file quietly saying the opposite of this page.
   - Next: "Once these are settled and you say it's right, I'll mark it
     Confirmed, and we can build the dated plan."
8. **On the owner's "yes, that's right"** ("confirm it", "that's
   everything"): if no clash is open, change the status line on the page
   itself to `Confirmed · YYYY-MM-DD`, then re-read it. Saying Confirmed in
   the reply while the page still says Draft is a failure. If a clash is
   still open, it stays Draft and the reply says which clash.
9. **Answers to open questions** fill a TBD or settle a clash. Answers are
   often short ("it's the 14th", "the date, not the day"): read every
   reply against the open clashes and TBDs on the page first, and take it
   as the answer to the one it fits. Only if it fits none, ask. File them
   on the page, add a change-log line (`TBD → value`), and re-run the checks.
   Then search the whole page for the old wording and fix every mention
   (an answer about the audience also changes "What this is" if it said
   "the whole list"). Standing facts in the answer follow rule 7. This is
   not *Changing a launch*: nothing else used the old value yet. If the
   answer creates a new clash, a Confirmed page goes back to Draft.
   Update the launch's STATE.md row too: status, today's date, and the
   real next step now (never leave the board asking a question the owner
   just answered; move a settled item out of Blocked).
   Run the *Settled elsewhere* search from step 7 again: answers often
   make a core file wrong (a start date in `core/offers.md`).
   **Open every update reply with this line, filled in:** "Updated your
   launch facts for [launch], in your launches folder under `[folder]`."
   Clearing an open question the owner just answered, or logging a
   decision they just made, follows the OS's own capture rules and is
   fine, but every file you touch outside this page gets one line in the
   reply ("Also: cleared the time-zone question, logged the list split in
   your decisions"). No silent moves (contract law 1). Anything else
   (a price in your offers file, another launch) is offered, not edited.

## Changing a launch

Use this when the owner changes a fact the page already had (not a TBD).

1. Change the value in `launch-facts.md`. Add a line to its *Change log*:
   date, what changed, old → new. Re-run the checks (step 3 of *New
   launch*) on the new value.
2. Search the whole OS for the old value (the exact link, date or price).
   List every hit in plain words and a few words of that line, one per
   line ("the invite email and Instagram post 1 in the drafted emails").
   Count only real hits. Skip the change log you just wrote.
3. List the places outside the OS that may still carry it. The OS can't
   fix these, so the owner has to hear them:
   - **Every partner on the page, by name**, when the change is to
     something partners promote (a link, a date, a price). They may already
     have the old value.
   - Emails already loaded or scheduled in the email tool, live pages, bio
     links, the event room.
4. Ask before editing any other file: "The old link is still in the
   drafted emails (the invite and Instagram post 1). Update those too?"
5. A Confirmed page stays Confirmed, since the owner stated the change,
   unless the checks found a new clash. Then it goes back to Draft until
   that's settled. Say so.
6. Reply in three parts, like this example:

   > **Changed:** the Pivot Week signup link is now …/pivot-week-2.
   > **Still on the old link here:** the invite email and Instagram post 1
   > in the drafted emails. Update those too?
   > **Outside the OS:** Marisol may already have the old link. Worth a
   > heads-up. Also check any scheduled emails and your bio link.

## Needs the owner's yes

- Marking the page Confirmed.
- Editing any file other than this page, STATE.md, and the standing-fact
  homes in rule 7 for something they just told you.
- Adding a new offer or a price change to `knowledge/core/offers.md`. Offer
  it; don't do it (contract law 9).

## Guardrails

- Nothing is sent, posted or scheduled. This skill only writes the facts
  page (contract law 4).
- Plain English in the reply. Say "your launch facts", "your offers
  file", "your standing rules". Every reply, a first draft or an update,
  says where the launch facts page lives once, in plain words, so the
  owner can open it.
- If the owner gives facts for two launches at once, make two pages and
  say so.
- Talk to the owner about their launch, never about this skill or its
  steps.
- End every reply with the next step. For a new launch: settle, confirm,
  then the calendar.
