---
name: leads
description: Keeps the owner's sales pipeline, the one table of everyone who might become a client. Logs leads (who, where they came from, what they're interested in), tracks each through fixed stages, keeps one next action and due date per open lead, shows who needs follow-up, flags leads that have gone quiet, and catches duplicates. Use when the owner mentions someone interested, a discovery or sales call, a new client, "who should I follow up with", "add her to my leads", or a brain dump of people they met. Also use when the owner mentions a new person in passing who sounds like a possible client: ask whether to add them. Keeps the pipeline in the owner's own tool when that tool is connected, and in a plain table in the OS when it isn't. It writes no messages and adds no one to any email list.
metadata:
  version: 2.0.0
  fitted-from: leads 1.1.0 (Jonathan's draft), fitted to the template 2026-09-29
---

# Leads — everyone who might become a client

One table so nobody falls through the cracks: who they are, where they
came from, where things stand, and the single next thing the owner does.

**Who owns what:** leads owns the pipeline. The follow-up skill drafts
personal messages to a lead. registrations tracks who's in an event.
`knowledge/core/offers.md` holds the offers and prices. Leads only points
to them. Nothing here is sent, and no one is added to an email list.

## Where the pipeline lives (one home, never two)

The owner should be able to open their pipeline and see it, in the place
they already work.

1. Check `knowledge/core/team-and-tools.md` for where clients and leads
   live (a CRM, ClickUp, Notion, a spreadsheet).
2. Check `connections/` for that tool's file. If the file says it's
   connected and what the OS may do there, **the tool is the pipeline.**
   Add and update leads there, within what the connection file allows,
   and keep no second copy in the OS.
3. If it isn't connected, or there's no tool, **the pipeline is
   `workspaces/pipeline/leads.md`**, a plain table the owner can open. Say
   once, the first time: "Your leads are in a simple table in your
   pipeline folder. If you'd rather keep them in [their tool], say 'help me
   connect [their tool]' and I'll walk you through it."
4. Never keep the same lead in two places. If a tool gets connected later,
   offer to move the table's rows into it, then mark the table as moved.

The rules below apply wherever the pipeline lives.

## Critical rules

1. **Only what the owner says.** Names, contact details, where they met,
   what they want: exactly as the owner gives them. Missing is
   `[Email needed]`, `[Last name needed]`. Never guess an email, a title,
   a company or anything else about a real person. Keep notes to what
   matters for the sale. No sensitive personal details the owner didn't
   ask to keep.
2. **Every open lead has exactly one next action and one due date.** Open
   means New, Contacted, Call booked or Offer made. The next action is one
   concrete thing the owner does: "send calendar link", "hold discovery
   call", "send proposal", "follow up on proposal", "check back after her
   review". Never two competing actions. For the due date, take the first
   of these that exists: a date the owner gave; the owner's own promise
   ("I said I'd send it tomorrow"); the lead's stated timing ("after the
   15th"); the owner's standing follow-up rule. Otherwise suggest one,
   marked `(suggested)`. Never present your date as the owner's. Never
   save an open lead without a next action: if the owner gave none,
   suggest the obvious one ("reply to her question about the Lab") with a
   date, both marked `(suggested)`, and say so.
3. **Fixed stages, moved only by evidence.** Stage is where the sale
   stands; the next action is what the owner does next. An activity alone
   doesn't move a stage. Use only these:
   - **New:** no real sales contact yet.
   - **Contacted:** the owner has had a real sales-related conversation
     or exchange with them.
   - **Call booked:** an actual sales or discovery call is on the calendar.
   - **Offer made:** the owner has actually presented an offer.
   - **Won:** the owner clearly says they became a client.
   - **Lost:** the owner clearly says it's not moving forward.
   - **Not now:** the lead asked to revisit later. Needs a check-back date
     (theirs, the owner's, or `(suggested)`). Any weekday you write next to
   a date, anywhere in the pipeline, is checked with a calendar tool
   first (for example `date -d 2027-03-02 +%a`); if you can't check it,
   leave the weekday off.
   If the owner's words don't clearly fit Won or Lost, ask.
   **Last contact** is the latest real sales-related exchange between the
   owner and the lead, not a note, an internal to-do or an automated email.
4. **Never merge people silently.** Same name, same email, or the owner
   seems to mean someone already there: ask "Same Rachel Kim as L001
   (from the mixer)?" Add or merge the new entry only after the answer.
   Don't hold up unrelated updates. But if the same message also brings in
   a second person with that name ("Rachel booked a call… also add Rachel
   Kim from the webinar"), even the update is unclear. Ask one question
   covering both, then apply everything on the answer.
   **Conflicting details:** if the owner gives a different email, phone,
   company or name for an existing lead, don't overwrite it silently. Ask
   whether the new one replaces the old. Keep the old value in History when
   it's replaced.
5. **No outside actions.** This skill records and organizes what the owner
   says. It never sends a message, books a call, registers anyone, charges
   or invoices (contract law 4). Writing a lead into the owner's connected
   pipeline tool on their yes is recording, not an outside action. Never subscribe anyone or say they've been added. If the owner wants a lead on the list, that's their email
   tool and the person's own consent. Say so once.
6. **Money is tracked, never charged.** On Won, note the offer and price
   only as the owner states them or as `core/offers.md` lists them,
   marked where each came from. Never infer which offer they bought:
   `[Offer needed]`, `[Price needed]`. No invoices, links or payments.
7. **History stays.** Every stage change is logged with its date. Lost and
   Not now leads stay in the table. Rows are never deleted. IDs (L001…)
   never change.

## Inputs

- The pipeline, wherever it lives (see *Where the pipeline lives*). In the
  OS: `workspaces/pipeline/leads.md` (create it from the template if it
  doesn't exist).
- The owner's message: a person, a brain dump, a call outcome, a question.
- `knowledge/core/offers.md`: offers and prices (for "interested in" and
  Won).
- `knowledge/core/business-profile.md`: the time zone.
- `knowledge/owner-profile.md`: any stated follow-up habits ("I follow up
  within 2 days").
- `knowledge/clients/`: to check a lead isn't already a client.

## What the owner can ask for

### Noticing a new person
When the owner mentions someone in passing who sounds like a possible
client ("I met a woman at the school gate who wants to go back to work"),
ask once, in one line: "Sounds like a possible client. Want me to add her
to your pipeline?" If the owner keeps leads in a tool that isn't connected
yet, say where she'd go in the same breath: "She'd go in a simple table
here for now, since Notion isn't connected. Say 'help me connect Notion'
any time." On a yes, add her below. On a no, drop it. Never add
someone the owner didn't say yes to.

### Add leads (one or a brain dump)
When the owner says "add Sarah" for someone not in the pipeline yet, add
them now with what you have (`[Last name needed]`, `[Email needed]`) and
say what's missing. Don't ask again whether to add them.
1. For each person: check for a possible duplicate first (rule 4).
2. Add a row with the next ID: source, interested in, stage (New, or
   Contacted if the owner already reached out), next action and due date.
   The owner's stated promise ("I said I'd send her my calendar link")
   *is* the next action.
3. Mark every missing detail `[… needed]`.

### Update a lead
Change the stage, last contact, next action and due as the owner says.
Log the change (date, old → new stage). A booked call gets its date,
time and time zone in the next action. Won: note offer and price
(rule 6). Lost: the reason, if given. Not now: a check-back date,
`(suggested)` if they didn't give one.

### "Who do I follow up with?" / what's due
Get today's date first. Group open leads:
- **Overdue:** due date before today.
- **Today.**
- **This week** (or the period asked for), soonest first.
- **Needs a next action:** open leads with none.
- **Gone quiet:** open leads with no contact in 14+ days (or the owner's
  stated number), unless a scheduled event explains the wait (a booked
  call, a date the lead set: "I'll decide after my review on the 30th").
  The owner's own reminder to check in doesn't count. That's the point of
  flagging. Also Not now leads whose check-back date has arrived.

Each lead appears once, in its most urgent group, with any other flag
noted on the same line ("due Mon Sep 28, and quiet 19 days"). For each:
name, stage, what's next, due, and the last contact. Check
weekdays with a calendar tool if you have one; if you can't check one,
leave it off. Offer the follow-up skill to draft any of these messages.

### Pipeline summary (when asked)
Count by stage and by source, and Won this month with offers. Count only
what's in the table.

## Every reply

Short and plain, about the owner's people, never about this skill or how
you decided. If the owner keeps leads in a tool that isn't connected, name
the tool and the sentence that connects it ("say 'help me connect
Notion'"). What changed, what's due, and questions (duplicates,
conflicting details, unclear Won/Lost, missing details). Say "your
pipeline", and say where it lives once, in plain words ("in your pipeline
folder" or "in ClickUp"). Check every weekday you write against a calendar
tool, or leave it off.

Before saving, re-check: every detail came from the owner (or
`core/offers.md` for offers), each stage is backed by what the owner said, each open
lead has one action and one due (suggested ones marked), duplicates were
checked, and old values are kept in History.

## Pipeline template (workspaces/pipeline/leads.md)

```markdown
# Leads — [Business name] pipeline

*Updated YYYY-MM-DD · Stages: New → Contacted → Call booked → Offer made → Won / Lost / Not now*

| ID | Name | Contact | Source | Interested in | Stage | Last contact | Next action | Due |
|---|---|---|---|---|---|---|---|---|
| L001 | Rachel Kim | [Email needed] | Denver leadership mixer, Sep 23 | Pivot Lab (maybe) | Contacted | Sep 23 | Send calendar link | Fri Sep 25 (suggested) |

## History
| Date | ID | Change |
|---|---|---|
| 2026-09-24 | L001 | Added (New → Contacted: talked at the mixer) |
```

## Needs the owner's yes

- Adding someone the owner only mentioned in passing (ask first).
- Merging two entries, or deciding two names are the same person.
- Marking a lead Won or Lost when the owner's words are unclear.
- On Won, starting a client file in `knowledge/clients/`: offer it, the
  shape the owner chose at onboarding (a roster or a file each).

## Guardrails

- Don't draft messages here. That's the follow-up skill.
- Don't register leads for events. That's registrations.
- Don't store payment details, ID numbers or health information.
