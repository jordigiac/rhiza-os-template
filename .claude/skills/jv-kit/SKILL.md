---
name: jv-kit
description: Assembles a ready-to-forward kit for each JV partner promoting a launch. Pulls the partner's tracking link, dates, commission and terms from the launch facts page, their send dates from the launch calendar, and the approved swipe copy from messaging, then checks every kit carries only that partner's link. Use when the owner asks for the partner kit, affiliate kit, swipe kit, JV packet, or "what do I send Marisol", when a partner's kit is due, or when a launch detail changes after kits went out. It writes no sales copy and sends nothing.
metadata:
  version: 2.0.0
  fitted-from: jv-kit 1.1.0 (Jonathan's draft), fitted to the template 2026-09-29
---

# JV kit — everything a partner needs, in one place

A partner should be able to promote the launch without asking a single
question. This skill compiles that kit, one per partner, from what the other
skills already produced. It checks the kit before the owner forwards it.

**Who owns what:** launch-facts owns the facts (links, dates, commission,
terms). launch-calendar owns when each partner sends and when their kit is
due. messaging owns the swipe copy and any talking points. jv-kit only
assembles, checks, and writes the short logistics cover note. It never
decides a fact, writes promotional copy, or edits the facts page, calendar or
drafts. If the owner gives a new fact, it goes through launch-facts first.

**When something upstream is wrong or missing,** jv-kit never corrects it
itself. It names the problem and the skill that owns the fix ("the facts page
has no tracking link for Kendra: launch-facts"; "no copy is matched to
J10: messaging"), keeps that kit a Draft, and moves on to the other kits.

## Critical rules

1. **One kit per partner, only their link.** A partner's kit contains their
   own tracking link from the facts page and no other partner's link. If the
   partner has no tracking link, the kit is a Draft: `[Tracking link needed]`.
2. **Link swap is the only change to approved copy.** In each swipe, a
   link to the offer or event (the registration page, sales page or
   checkout from the facts page) is replaced with this partner's tracking link.
   Everything else stays exactly as messaging approved it: subject lines,
   wording, length, tone, claims, CTAs. No rewriting, trimming or
   polishing. If the copy has a link you can't safely identify, or
   *another partner's* tracking link (a sign it was written for someone
   else), don't swap it. Flag it for messaging.
3. **Facts match the facts page exactly in meaning.** Event name, dates, times
   with time zone, commission, payout timing, refund window, credit rules.
   Layout may change for readability ("Tue Nov 10, 12:00pm MT" can become
   a table row). The values themselves never change and are never
   inferred. Links, prices and percentages stay character for character.
   A missing term shows as `[Payout timing needed]`, never a guess or a
   "usual" value applied silently.
4. **Each send gets its own copy, matched by ID.** Every partner send row
   in the calendar (J07) maps to the messaging section with the same ID,
   and that goes into the matching kit section. Never use copy from another
   send because it's for the same partner. If a row has no matching copy,
   or the match is unclear (no ID, two candidates), flag it. If the copy
   isn't Approved, the kit is a Draft. Don't write copy here.
5. **Keep the disclosure.** Every swipe keeps its commission disclosure
   line. If one is missing, the kit isn't ready. Ask messaging to add it.
6. **Match the channel.** Each send gets what its channel needs: emails
   for a list, talking points for a podcast, a caption for social. A
   partner with sends on several channels gets each in its own format,
   send by send. If messaging hasn't written the right format, flag it.
   Don't improvise one.
7. **Sent kits are history.** Once the owner says a kit went out, it's never
   rewritten. Changes go in a dated *Update* section (see below).
8. **Nothing is sent.** The owner forwards the kit. Commissions are tracked,
   never paid or charged here.

## Inputs

- `workspaces/launches/<launch>/launch-facts.md`: partners, contacts,
  commission, tracking links, send windows, terms, event and offer facts.
- `workspaces/launches/<launch>/calendar.md`: the partner rows (J…):
  kit due date, send dates, what each send promotes.
- `workspaces/launches/<launch>/messaging.md`: swipe copy and talking
  points for those rows, with their status.
- `workspaces/launches/<launch>/partner-kit.md`, if it exists: kits
  already built or sent.
- `knowledge/partners/<name>.md`, if it exists: how this partner likes to
  be asked, and what they needed last time. Tone for the cover note only;
  never a fact that isn't on the facts page.
- `knowledge/core/voice-samples.md` and `knowledge/core/voice.md`: the
  owner's voice, for the cover note.

## Steps

1. **Find the launch and the partners.** Read the three files. If the
   owner approves the partner's drafted swipe copy in the same message
   ("Approved. Build Priya's kit."), record that first: Status → Approved,
   dated, in the drafts and in the calendar row, the way messaging does.
   Recording the owner's yes is not rewriting copy. Never hand back an
   approval they just gave. If the
   facts page has no partners, say so and stop. If the calendar has no partner
   rows, say the calendar needs them first.
2. **For each partner, gather:**
   - Logistics from the facts page: event and offer names, dates and times
     with time zone, their tracking link, commission, payout timing,
     refund window, anything else the facts page states about partner terms.
   - Their schedule from the calendar: kit due date, each send date and
     what it promotes.
   - Their copy from messaging: the swipe or talking points for each of
     their send rows, and each row's status.
3. **Build the kit** from the template below: the cover note, the schedule,
   the terms, the links, then the copy for each send, by row ID.
   **The cover note** summarizes the logistics and says what to do next, in
   the owner's voice. Every fact in it comes from the facts page or calendar. It
   adds no claims, testimonials, urgency, promises or persuasion; that's
   messaging's job.
4. **Check every kit before saving:**
   - The only link in it is this partner's tracking link, character for
     character from the facts page. Tables and the cover note name pages
     in words ("Registration page", "Sales page"), never as a URL. After
     saving, search the kit for the owner's domain and for "http": every
     hit must be this partner's tracking link. A plain link in a kit can
     cost the partner credit for the sales they drove.
   - Every date, weekday, time and zone matches the facts page and calendar.
     Check weekdays with a calendar tool if you have one; if you can't
     check one, leave it off.
   - Each send date sits inside the partner's window, and before the event
     or cart close.
   - Every swipe has its disclosure line.
   - Every gap is a visible `[… needed]` placeholder.
   - The cover note passes the quality check: the Gate (`evals/gate.md`),
     the voice check (`evals/standard/voice-check.md`), then the humanizer.
     The approved swipe copy is not re-run through the humanizer; it stays
     exactly as the owner approved it (rule 2).
   **Ready** only when all of these hold:
   - every partner fact the kit uses is in the facts page (no `[… needed]` left),
     including where the kit goes (the partner's email or handle)
   - the partner's tracking link is present and passed the link check
   - every send row has matching copy, by ID, in the right format
   - all that copy is Approved and has its disclosure line
   - every date check passed

   `[your name]` / `[your story]` fill-ins are left for the partner and
   don't block Ready. Anything else is **Draft**. List *every* reason under
   *Still needed*, each with the skill that fixes it.
5. **Save** all kits to `partner-kit.md` in the launch folder, one section per
   partner. Keep earlier sections and updates.
6. **Reply briefly.** Say "the kits" and "the drafts", and say where the
   kits live once, in plain words ("they're in the launch folder, one
   section per partner"). Give each partner, Ready or Draft, and what's
   missing; the
   kit due dates, soonest first (flag any already past); what the owner does
   next ("Forward Marisol's kit by Tue Oct 13, then tell me it's sent").
   Every weekday in the reply is checked against the calendar, including
   relative ones ("this Friday"). If you can't check it, give the date
   without a weekday.
   If a partner's send rows have no swipe copy yet, say so plainly and
   offer to have it drafted. Never stand in with the owner's own list
   emails or a note to the partner.

## When the owner says a kit went out

Note it in that partner's section: `Sent YYYY-MM-DD`. The facts page's *Kit
sent?* column and the calendar's kit row are updated through launch-facts and
launch-calendar, so both stay the single record. Offer, once, to add a line
to that partner's file in `knowledge/partners/` ("kit sent for Pivot Lab,
Nov 2026"), so the next launch knows the history.

## When something changes after a kit went out

1. Leave the sent kit exactly as it was.
2. Add a dated **Update** section under that partner's kit: what changed
   (old → new), which of their sends it affects, what they need to do
   ("swap the link in both emails before Oct 27"), and the corrected copy
   if the copy was affected (from messaging, with the link swap only).
   This covers link, date, commission and term changes alike.
3. Earlier Updates stay exactly as written. For each fact, the latest
   Update is the one in force; say so in its first line ("Replaces the
   Oct 2 update on the link").
4. Only partners whose kit carried the old value get an update. When the
   owner says an update went out, note `Update sent YYYY-MM-DD` in it.
5. Put these first in the reply, with each partner's next send date.

Kits not yet sent are simply rebuilt.

## Kit template (one section per partner in partner-kit.md)

```markdown
## Marisol Grant — Pivot Week (Nov 10–12, 2026)
*Status: Draft / Ready / Sent YYYY-MM-DD · Kit due: Tue Oct 13 · Built from the facts page's YYYY-MM-DD version*

### Cover note
[short logistics note to the partner, in the owner's voice]

### Your dates
| When | What to send | Promotes |
|---|---|---|
| Tue Oct 27 | Email 1 | Registration page |

### Your link
[their tracking link, from the facts page]

### Terms
- Commission: … · Paid: … · Refund window: …

### The copy
#### Email 1 (Tue Oct 27)
[approved swipe from messaging, with their link]

### Still needed before this is ready
- … or (nothing)
```

## Needs the owner's yes

- Forwarding any kit (the owner sends it).
- Any partner term that isn't in the facts page.

## Guardrails

- Plain English in the reply. Say where the kits live once, in plain words.
- Nothing is sent (contract law 4). The owner forwards every kit.
- Never put two partners' details in one kit.
- Don't write swipe copy, subject lines or talking points. That's messaging.
