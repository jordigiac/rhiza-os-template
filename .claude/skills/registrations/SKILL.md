---
name: registrations
description: Keeps the roster for each paid or free event, workshop or program round. It records who's registered, what option they chose, what they owe and have paid, invoices, seats against the cap, the waitlist, refund requests against the refund policy, partner-referred sales, and attendance afterward. Use when the owner says someone signed up, paid, wants a refund, is coming free, asks who's in or who still owes, pastes a registration or payment export, or marks attendance. It tracks money and never charges, refunds or invoices anyone.
metadata:
  version: 2.0.0
  fitted-from: registrations 1.1.0 (Jonathan's draft), fitted to the template 2026-09-29
---

# Registrations — who's in, who's paid, who still owes

One roster per event. The owner always knows who's coming, what was
collected, what's still owed, and how many seats are left, without
digging through their payment tool.

**Who owns what:** launch-facts owns the event's facts: options, prices,
payment plan, early bird deadline, seat cap, refund terms, JV partners and
commission rates. registrations owns the roster and what the owner reports
about payments. leads owns the sales pipeline (someone who registers can be
marked Won there, but only by the leads skill). Payment reminder and
follow-up messages come from the follow-up skill. The payment tool (Kajabi,
Stripe, Venmo) is the real record of money. This roster is the owner's copy.

## Critical rules

1. **Money is recorded, never moved.** Record payments, refunds and invoices
   only as the owner (or an export they paste) states them: amount, date,
   method ("Venmo", "Kajabi"). Never charge, refund, invoice, send a
   reminder, or say any of these happened. Never mark someone paid because
   they registered. Invoice status too is only what the owner or export says.
   Every money event (payment, installment, refund, denial) is its own dated
   line in the Log. Earlier lines are never erased. A refund doesn't delete
   the payment it refunds.
2. **Prices come from the facts page.** What someone owes comes from the option
   they chose, at the facts page's price. If it's unclear which applies (early
   bird timing, several options, which option they picked), show the
   choices: `[Price needed: $147 if paid by Sat Oct 3, else $197]`. Never
   pick one to make the math work. Payment plans: record each installment
   (amount, date, method), what's left, and the next due date only if the
   facts page or owner gives it. Never invent a schedule.
   **Comp** only when the owner says the person attends free (note their
   reason if given). A friend, a partner, or a missing payment isn't Comp.
3. **Only what the owner says about people.** Names, emails, how they heard:
   as given. `[Email needed]` when missing. Store no card numbers, bank
   details or anything sensitive.
4. **Seats are counted, never oversold.** An active seat is Seat =
   Registered with any payment status except Refunded (Unpaid, Partial,
   Paid and Comp all count). Waitlist, Cancelled and Refunded don't count.
   At the cap, new people go on the Waitlist, in the order they were
   added, and the owner is told. Nobody moves up or off the waitlist
   unless the owner says so, not even when a seat opens.
5. **Refunds follow the owner's policy, and the owner decides.** Check a
   request against the facts page's refund terms and say whether it looks inside
   or outside them, with the date. Record it as Refund requested. The seat
   stays active. Mark it Refunded only when the owner says they refunded,
   with amount and date. Then ask whether the seat is Cancelled (usually
   yes). If the owner denies it, log the denial and set payment back to
   what it was.
6. **No duplicates, no forced matches.** Match people by email first, then
   name. A possible match is asked about ("Same Beth as R004?"), never merged
   silently. Every incoming payment is sorted as **matched** (clearly this
   person, and the amount fits: record it), **possible match** (flag it for
   the owner) or **unmatched** (no reliable person or no clear link to this
   event, like a Venmo "$147 from S.L.": keep it in *Unmatched payments*,
   flagged). An order or checkout row for this event, with the buyer's name
   and email, *is* a registration. Add it, marked "new from export". Never
   create a registration to explain a payment that isn't one. A payment
   already in the Log (same person, amount, date) isn't counted again. Two
   identical charges in one export are counted once and flagged as a
   possible double charge for the owner to check in the payment tool.
7. **The three statuses are independent.** Seat, Payment and Attended never
   change each other automatically. Registered + Unpaid + No-show is a
   real combination. A no-show isn't cancelled, refunded or moved. Attended
   and No-show are recorded only as the owner gives them.
8. **History stays.** IDs (R001…) never change. Cancelled and refunded
   people stay on the roster. Every money change is logged with its date.

## Three short status columns

- **Seat:** Registered · Waitlist · Cancelled
- **Payment:** Unpaid · Partial (paid 1 of 3) · Paid · Comp · Refund requested · Refunded
- **Attended:** — (before the event) · Attended · No-show

## Where the roster lives

Every event is a launch, even a small one-off workshop, so the roster sits
in that launch's folder: `workspaces/launches/<launch>/registrations.md`,
beside its `launch-facts.md`. Prices, options, cap and refund terms come
from that facts page. If the event has no launch folder yet, say so and
offer to start its facts page first (launch-facts). Create the roster from
the template if it doesn't exist.

**If the owner's registration or payment tool is connected** (a file in
`connections/` says so), the roster can be filled from it on the owner's
ask, read-only, within what that file allows. The tool stays the real
record of money; the roster stays the owner's one readable copy. If it
isn't connected, the owner pastes an export or tells you, and the roster
says once where it lives.

## What the owner can ask for

### Pasted export (registrations or payments)
Sort every row before changing anything: new registrations; payments that
match someone; possible matches; unmatched payments; duplicates (a row
already recorded, or the same transaction twice in the export); amounts
that don't fit any option; refunds. Apply only the reliable ones. Report
the rest in groups, so the owner can settle each.

### Add or update people
From a message: for each person, check duplicates
(rule 6), then add or update the row. Option and amount owed come from the
facts page (rule 2). Record source when given ("Kendra's link"), since it matters
for partner commissions. Payment plan: track installments (paid 1 of 3,
next due date if the facts page or owner gives the schedule). A payment date in
the future, or an amount that doesn't match any option, is flagged and
asked about. Don't fix it.

### Roster summary ("who's in?", "where are we?")
- Seats: active / cap, seats left, waitlist count.
- Money (show the math): collected so far; still owed (unpaid and
  remaining installments); comps; refunds requested and done.
- Partner commissions: the amount each partner-referred buyer actually
  paid (recorded payments only, minus any refund) × the facts page's rate =
  owed to that partner (tracked; the owner pays; Paid only if the owner
  says so). If a rate is missing, say so.
- Who still owes, soonest due first. Invoices needed or outstanding.

### Refund request
Check the policy (rule 5), record Refund requested, tell the owner whether
it's inside the terms, and note that the seat frees up only once it's
Refunded or Cancelled (and who's first on the waitlist, if anyone).

### Attendance (after the event)
Mark Attended / No-show per person as the owner gives it. Follow-up uses
this.

## Every reply

Short and plain: what changed, the seat count, the money summary if it
moved, and questions (duplicates, unclear prices, flags). Say "the
roster", and say where it lives once, in plain words ("in the launch
folder, next to the launch facts"). Nothing is charged, refunded or
invoiced (contract law 4). Before saving, re-check: every amount
came from the owner or an export, every price owed from the facts page, nothing
counted twice, unmatched payments still flagged, the math adds up, seats
are counted per rule 4 and the cap isn't exceeded, waitlist order is
unchanged, and nothing was marked paid, refunded or invoiced without the
owner saying so.

## Roster template (registrations.md)

```markdown
# Registrations — [Event name]

*Event: [date, time, zone] · Cap: [n] · Options: [from the facts page] · Refund terms: [from the facts page] · Updated YYYY-MM-DD*

| ID | Name | Email | Option | Owes | Paid | Seat | Payment | Attended | Source | Invoice |
|---|---|---|---|---|---|---|---|---|---|---|
| R001 | Priya Shah | priya@shah.io | Early bird | $147 | $147 · Sep 20 · Kajabi | Registered | Paid | — | Webinar | n/a |

## Summary
- Seats: … / … · Waitlist: …
- Collected: … · Still owed: … · Comps: …
- Partner commissions (tracked): …

## Waitlist
| Order | Name | Email | Added |
|---|---|---|---|

## Unmatched payments
| Date | From (as shown) | Amount | Method | Why unmatched |
|---|---|---|---|---|

## Log
| Date | ID | Change |
|---|---|---|
```

## Needs the owner's yes

- Approving a refund, comp, or waitlist move.
- Merging two people.

## Guardrails

- Don't send payment reminders. The follow-up skill drafts those.
- Don't change prices, cap or refund terms. They belong to launch-facts.
- Don't store payment card or bank details.
