---
name: launch-calendar
description: Builds and updates a launch's dated plan from its facts page. Covers every email send (date, time, who gets it, who's excluded, which link), social posts, each JV partner's send dates and kit deadline, and the backwards-planned setup deadlines (pages tested, emails loaded, partner kits out). Checks for past dates, too many emails in a day, holidays, partners mailing after close, and clashes with promos the owner promised others. Use when the owner asks to plan, map out, or schedule a launch, asks when emails or partner sends go out, asks what's due this week for a launch, or when a launch date moves and the plan needs redoing. Use it right away, even when the facts page is still a Draft or has gaps: it plans what it can and marks what's waiting. Reads the facts page from launch-facts; the copy for each send comes later from messaging.
metadata:
  version: 2.0.0
  fitted-from: launch-calendar 1.2.0 (Jonathan's draft), fitted to the template 2026-09-29
---

# Launch calendar — the dated plan everyone works from

The facts page says *what* the launch is. The calendar says *what happens on which
day*: every send, every post, every partner mailing, every setup deadline.
It writes no copy. Each send gets an ID (E01, P01…), and messaging writes the
copy against those IDs later, taking the date, audience and link from the
row instead of working them out again.

**Who owns what:** launch-facts owns the facts (offer, dates, times, links,
audience, partners). This skill owns the plan: which send goes when, to whom,
and what's due. messaging owns the copy. The calendar never sets or
overrides a launch fact. If the calendar and the facts page disagree, the facts page
wins and the calendar gets rebuilt.

## Critical rules

1. **The facts page is the only source.** Every date, time, link, email group,
   and partner comes from `launch-facts.md`. Refer to links by name ("Registration
   page"), never by retyping the URL. If the owner gives a launch fact while
   you're planning ("actually cart closes the 18th"), don't edit the facts page
   silently. Hand it to launch-facts' process: an answer to a TBD is filed
   and logged, a change to an existing fact goes through its change steps
   (which may flag other drafts and partners). Then rebuild the calendar
   from the updated facts page (update mode).
2. **Never plan from a TBD.** A send that depends on a TBD fact is written
   with `TBD` in that field and listed, with its ID, under *Waiting on the
   facts page*. No guessed dates or times. A Draft facts page makes a Draft calendar;
   it never makes a finished one.
3. **Nothing new in the past.** No planned send, post, or deadline before
   now. (Loaded and Sent rows keep their dates, see rule 6.) If the
   timeline is too short for a default (a partner kit that needed 14 days),
   flag it. Don't quietly shrink it.
4. **Fixed vs suggested.** Every date and time in the plan is a suggestion
   the owner can change, *unless* it follows straight from a settled facts page
   fact (cart opens at 1:15pm, the live starts at noon, "15 min before the
   noon live"). Mark those `(fixed)`. A facts page value still marked
   unconfirmed or `(confirm)` is never `(fixed)`. Mark it `(unconfirmed)`.
   Don't mark suggested dates and times; the calendar header says so once.
   Things you add that the owner didn't ask for (a task owner, a correction
   send) are marked `(suggested)`. Never present a suggestion as the owner's
   decision.
5. **Every send names its audience.** Each row has *To* and *Exclude*. The
   facts page's exclusions go on every dated email row (automation and social
   rows follow step 8). From the cart-open email on (it counts as a sales
   send), every sales send also excludes the buyer tag (or `buyer tag TBD`).
   If the owner's email groups aren't on file anywhere (no *Your email list*
   section in `knowledge/core/audience.md`, and the facts page says TBD),
   ask once, the way launch-facts does: "How do you split your email list,
   and is there anyone who should never get a sales email?" File the answer
   in that section in their words, say so in one line, and plan with it.
   Until then, *To* is `TBD`.
6. **Never move what already went out.** Rows marked Loaded or Sent are
   locked: their date, time, audience and status stay as recorded unless
   the owner or team says to change them. Only the owner or team marks a row
   Loaded or Sent. When a changed fact affects a locked row, flag the
   real-world fix (edit it in the email tool, send a correction). Don't
   rewrite the record.
7. **IDs never change.** Once a row has an ID, it keeps it, because messaging
   and the owner's email tool refer to it. New rows get the next unused
   number (even if out of date order). A row that's no longer needed stays,
   with status `Cancelled`.
8. **Plan only.** No copy, nothing scheduled in any tool, nothing sent.

## Inputs

- `workspaces/launches/<launch>/launch-facts.md`: the facts. Read its status
  and *Still TBD* first.
- `references/launch-patterns.md` (in this skill's folder): the default send
  pattern for each launch type, the JV rhythm, and backwards setup deadlines.
  Read the section for this launch's type.
- `knowledge/core/business-profile.md`: the time zone.
- `knowledge/core/team-and-tools.md`: the team (who owns tasks) and the
  channels the owner actually uses.
- `knowledge/core/audience.md`, the *Your email list* section: the owner's
  email groups.
- `knowledge/owner-profile.md`, `CONTRACT.md` and `decisions.md`: standing
  sending rules (e.g., "never email on Sundays").
- `knowledge/partners/`: promos the owner promised to send for other
  people's launches, if any are written there.
- `workspaces/launches/<launch>/calendar.md`, if it exists: the current
  plan (update mode).

## Steps

1. **Find the launch.** If the owner didn't name it and more than one launch
   is active, ask which. Get today's date and a reliable calendar for every
   month from today through cart close, using whatever the host provides
   (in a terminal, for example: `date "+%a %F"; cal 11 2026`). Read every
   weekday you write off that calendar, today's included. Never work
   weekdays out in your head. If you can't check a date, write it without a
   weekday.
2. **Read the facts page.** If it's still Draft, say so in one line and continue:
   A Draft facts page gets a Draft calendar with its gaps marked. Note any times
   in the facts page not in the owner's time zone. Flag them; don't convert them
   silently.
3. **Lay out the key dates** from the facts page: promotion starts, event day(s),
   cart opens, early bird ends, cart closes, each partner window.
4. **Build the send plan** from the pattern for this launch type, adjusted
   to the real dates. Build around the owner's standing rules from the start
   (no send on a day they never send). Don't place a send there and then flag it.
   If the runway is shorter than the pattern needs, keep the core sends (see
   *Short runway* in the reference), drop the optional ones, and say which
   you dropped. One row per send, in date order:
   emails `E01…`, social posts `P01…` (only for channels the owner uses).
   Include the automation emails (confirmation, welcome) as rows with Date
   `on signup` / `on purchase`, so nothing gets forgotten.
5. **Build the partner plan.** For each JV partner: kit due (14 days before
   their first send; if that date has passed, the kit is due today, flagged
   as late), a reminder the day before their first send, their send
   dates inside their window, what they promote (the link name), and their
   tracking link. Rows `J01…`.
6. **Build the setup deadlines** by working backward from the sends (see
   the reference): pages tested, emails loaded, room tested, checkout and
   buyer tag tested, replay page up. Each deadline lands before the *first*
   send that needs it (the first replay email, not the last). A task that
   covers several sends ("load E16–E22") is due 2 days before the earliest
   of them. Rows `T01…`. Suggest an owner from the
   team in `knowledge/core/team-and-tools.md`, marked `(suggested)`.
   **Fit the owner's week.** Read how their week runs
   (`knowledge/owner-profile.md`, and "How the work usually flows" in
   `team-and-tools.md`). Setup tasks land on their working days, never a
   day they keep free. A task that needs writing or loading emails lands
   on their writing or admin day if they have one, the latest such day
   before its due date. Say so in the reply when you moved one.
7. **Check the whole plan** and write each problem under *Flags*:
   - Any date before today, or any weekday that doesn't match its date.
   - Any time without the owner's time zone, or in a different one.
   - More than one promotional email to the same audience on a day (except
     event days and close day, max 3).
   - A send after cart close, or a partner send outside their window or
     after close.
   - Major public holidays in the owner's country within 2 days of any key
     date or of the first invite (in the US: Thanksgiving, Black Friday and
     Cyber Monday, Christmas, New Year's, July 4, Memorial Day, Labor Day).
     Inboxes are crowded and people are away. Flag it; don't move it. Work
     out the holiday dates for this year from the calendar first (e.g.
     Thanksgiving = 4th Thursday of November; Black Friday is the next day,
     Cyber Monday the Monday after), then compare them to *every* key date
     and the first invite.
   - Owner's standing sending rules broken (e.g., a Sunday send).
   - A setup task or kit deadline on a day the owner doesn't work.
   - Promos the owner promised to send for someone else (from
     `knowledge/partners/`) that land in this launch's window. The owner
     would be mailing for someone else during their own launch.
   - Setup deadlines already past or too tight.
   Fix what's yours to fix (a slot you chose). Flag what's the owner's call.
8. **Check every row before you save.** Go down the table one row at a time:
   - Its weekday matches its date on the calendar, and it's not before
     today. When you moved a row (to today, off a Sunday), its weekday
     moved too. Rewrite it from the calendar.
   - It isn't on a day the owner's rules forbid (a Sunday, if they never
     send on Sundays). Move it to the nearest allowed day, and say so in Flags.
   - Its Exclude cell starts with the *Always exclude* line, copied exactly,
     on every dated email row, registrant rows included (never `—`).
     Automation rows (on signup / on purchase) go to the person who just
     acted: Exclude = `n/a (triggered by signup)`. Social post rows:
     To = `followers (public)`, Exclude = `n/a (public post)`. Add the buyer
     tag if the row is on or after cart open.
   - Nothing lands after cart close. Partner rows sit inside their window.
   - No audience gets two promotional emails in a day (event and close days
     aside).
   - The same goes for every date in *Flags* and in your reply. Never
     write a weekday you haven't checked. If you can't check it, leave the
     weekday off.
   Fix and check again until every row passes.
9. **Write `calendar.md`** in the launch folder, using the template below.
   Put the facts page's *Last updated* date in the header so a stale calendar is
   easy to spot. **Then verify the saved file:** list every distinct date in
   it and check them all against the calendar in one go (in a terminal, for
   example `for d in 2026-12-02 2026-12-09; do date -d $d "+%F %a"; done`).
   Fix every weekday that doesn't match, and check the first cart-open row
   excludes the buyer tag. Run the truth check
   (`evals/standard/truth-check.md`) on the saved plan: every date, link
   name and audience traces to the facts page or knowledge/.
10. **Update STATE.md**: in the launch's Active row, set the next step
   ("calendar drafted; okay the plan, then the emails").
11. **Reply briefly.** Open with one line like "Calendar drafted for Pivot
    Lab, November. It's next to the launch facts, in the same folder." Say
    "the calendar" and "the facts page", and say where it lives once, in
    plain words. Then give:
    - The counts: emails, posts, partner sends, setup tasks.
    - **Next 3 deadlines.** Work these out from the saved calendar *before*
      you start writing the reply: take every dated row from all three
      tables (sends, partner plan, setup), sort by date, and keep the first
      three from today on (a partner kit due date counts). Write the list
      once, already sorted. Never correct yourself mid-reply.
    - **Flags (each needs your answer):** one line each, written as a
      question the owner can answer in a word or two ("Dana's email isn't
      on file and her kit is due Sun Oct 4. Where should it go?"). Never a
      bare statement.
      A flag with nothing for the owner to decide isn't a flag: put it under
      what's waiting on the facts page instead.
    - Anything waiting on the facts page, most urgent first. Anything that
      blocks the next deadline (a partner's contact, a missing link) is
      always on this list.

    Always end with: "Once the plan looks right (and the waiting items are
    answered), messaging can write the copy for each send."
12. **On the owner's okay** ("the plan looks good"), set the calendar's
    status to Approved, dated. Never while the facts page is still Draft. Say
    the facts page needs confirming first.

## When the facts page changes (update mode)

1. Compare the facts page's *Last updated* date with the calendar header. Read
   the facts page's change log to see exactly which facts changed. An Approved
   calendar goes back to Draft until the owner okays the new plan.
2. **Locked rows first.** Rows marked Loaded or Sent stay exactly as they
   are in the calendar. But for each one, ask: does its copy likely mention
   a fact that changed (a date, time, price, link, deadline)? If yes, it is
   the most urgent flag: "E01 is loaded in your email tool with the old
   dates (Nov 10–12). Edit it there before it sends Mon Oct 26." For a Sent
   row, suggest a correction send (a new row, `(suggested)`).
3. Recompute every Planned and Drafted row from the new facts, keeping
   their IDs (rule 7). Drafted or Approved rows that moved go back to
   Planned, because their copy mentions the old dates. Name them.
4. Re-run the checks (step 7) and the row-by-row check (step 8) on the
   whole plan, including partner windows against the new dates.
5. Reply in this order: (a) locked rows that need fixing in the email tool,
   with the date they send; (b) what moved, one line per row, or grouped
   when many moved the same way ("E03–E24: all +7 days"); (c) Drafted rows
   sent back to Planned; (d) other flags, each ending in a question;
   (e) the next 3 deadlines, worked out exactly as in step 11 (every table,
   sorted, from today on, partner kits included).

## Calendar template

```markdown
# Launch calendar — [Launch name]

*Status: Draft (or Approved, date) · Built from the facts page's YYYY-MM-DD version (facts page: Draft/Confirmed) · Calendar updated YYYY-MM-DD*
*All times [owner's time zone]. Dates and times are suggestions you can change, except those marked (fixed), which come from the facts page.*

## Key dates
- Promotion starts: …
- Event: …
- Cart opens: … / Early bird ends: … / Cart closes: …
- Always exclude (every row): [the facts page's exclusions] · Buyer tag (every row from cart open): […]

## Send plan
| ID | Date | Time | Channel | To | Exclude | Purpose | Link | Status |
|---|---|---|---|---|---|---|---|---|
| E01 | Mon Oct 26 | 7:00am | Email | newsletter, quiz-takers | past-pivot-lab | Invite 1 | Registration page | Planned |

## Partner plan
| ID | Partner | Date | What | Link | Status |
|---|---|---|---|---|---|
| J01 | Marisol Grant | Tue Oct 13 | Kit due to partner | Tracking link | Planned |

## Setup deadlines
| ID | Due | Task | Owner | Status |
|---|---|---|---|---|
| T01 | Fri Oct 16 | Registration page live + every link clicked | Priya (suggested) | To do |

## Flags
- one line each, with the question to settle it

## Waiting on the facts page
- each TBD that blocks a row, and which rows
```

Status words. Sends and partner rows: Planned → Drafted (copy written by
messaging) → Approved (the owner okayed the copy) → Loaded → Sent, or
Cancelled. Setup rows: To do → Done. The calendar itself: Draft →
Approved.

## Needs the owner's yes

- Changing anything in the facts page (that goes through launch-facts).
- Saving a new standing rule the owner states ("I never email on Sundays")
  to `knowledge/owner-profile.md`. Offer to; don't do it silently.
- Marking anything Loaded or Sent, or changing a locked row.
- Approving the calendar.

## Guardrails

- Plain English in the reply. Say "the facts page", "the calendar", "your
  team", and where the calendar lives once, in plain words. Never talk
  about this skill or its rules.
- Nothing is scheduled or sent (contract law 4).
- Keep the purpose column to a few words ("Invite 2", "FAQ", "Closing
  today 1/3"). The copy belongs to messaging.
- One calendar per launch. Never mix two launches in one file.
