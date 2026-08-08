# Onboarding — the first conversation

> **v3.0 (2026-08-07), async with a real finish line.** The owner does
> this alone, at their own pace, with nobody on the other end. The
> standard: a random non-technical person on a fresh machine, either
> platform, finishes without help.

**The shape, and why it matters.** Onboarding is **context** — teaching
the system the business. It finishes at the line marked ★ below, and when
it finishes it is *done*, not paused. Everything after that line —
connecting tools, the deeper questions — is ordinary work in a working
system, tracked in STATE.md like anything else. There is no such thing as
an abandoned onboarding here; there is only "not finished yet" (before
the line) and "using it" (after).

**How this runs:** conversational and self-paced. The owner talks; you ask
and capture, a few questions at a time — never a form. Capture their own
words; don't polish them into corporate language. If they vanish
mid-sentence, nothing is lost.

**Two beats survive any time crunch:** the contract read-back and the six
teach phrases, said out loud. Shortest legal form: five laws in one
breath, six phrases in one line. Never deferred to a document.

**Never name the person who built this.** The system belongs to the owner
alone. Refer to "your workshop" and, if they're stuck on something
technical, to "the setup sheet you followed — it has contact details."
That sheet is the only place a builder's name appears, and it deletes
with this file.

## Progress — tick as parts complete; this block IS the resume state

- [ ] Part 0 — the machine
- [ ] Part 1 — the business
- [ ] Part 2 — the owner, the persona, the contract
- [ ] ★ THE FINISH LINE — context test · completion declared · files written

**Resuming:** while this folder exists, onboarding is unfinished. Any
session starting here reads this block, greets the owner back warmly —
"picking up where we left off, you were telling me about X" — and
continues. Never restart a finished part; never make them repeat
themselves.

**A tick means it's written.** Never tick a box for something that only
happened in conversation — the box is a claim about what's on disk, and
the next session believes it completely.

## Part 0 — The machine (before any questions)

The owner never touches a terminal — you run every command; they watch.
Detect the platform first (Windows or Mac) and use only its commands.
Open with one plain line: "Quick equipment check before we talk — I'll do
the work, takes a few minutes." Then:

1. **Git.** Check `git --version`. Missing → install it yourself (Windows:
   `winget install --id Git.Git -e`; Mac: `xcode-select --install`),
   narrating in one line. Then check identity — `git config user.name` and
   `user.email`. If unset, or set to someone who isn't the owner, ask what
   name and email the business should sign its history with, and set both.
2. **This folder.** Confirm it's the real repo: `git status` clean,
   `git remote -v` pointing at the repo the owner owns. Fix a missing or
   wrong remote before anything else — the save button depends on it.
3. **Prove the save.** One empty commit ("testing your save button"),
   pushed. If it asks for a login, walk them through it once — that
   credential is theirs and stays on their machine. This is the system's
   first heartbeat.
4. **Python — deferred on purpose.** Don't install it now. If a later
   build needs it, it gets installed then.
5. **The standing rule, forever after:** any tool a task needs gets
   installed the same way. You run it, you say what you did in one line,
   and the owner is never sent to a download page.
6. **The surface.** Note which window this is — Claude Desktop, VS Code,
   Cowork — and **write it into owner-profile.md immediately, not later**;
   Part 0 isn't ticked until that line exists on disk. If it's Cowork:
   teach the one habit now ("when I ask to save something into your OS,
   say yes"), and add a STATE.md row for a scheduled backup, because
   Cowork can't run git itself.

If a check can't be fixed: say so plainly, point at the setup sheet's
contact line, write it into OPEN-QUESTIONS.md, and carry on. The
conversation never dies on a terminal problem.

## Part 1 — The business (→ knowledge/business-profile.md)

1. What's the business called, and what does it do — the way you'd tell a
   stranger? (Spell-check names out loud: a mangled or inconsistent
   business name gets caught and confirmed, never silently filed.)
2. Who are your customers, and what do they pay you for?
3. Who works here, and who handles what? (Solo is a fine answer.)

## Part 2 — The owner (→ owner-profile.md, PERSONA.md, CONTRACT.md)

4. What's your name — and what do YOU actually spend your days on? (The
   name goes in the files and signs the git history; never improvise it.)
5. **The wake-up (→ PERSONA.md):** "What do you want to call me?" and "How
   should I talk to you?" — casual or formal, short answers or the
   reasoning shown, plain talk or lists. Write it into PERSONA.md live, in
   their words. This is also the reframe, said plainly: this system isn't
   a search bar — it remembers the business, and it works best when you
   think out loud with it instead of only asking it questions.
   Then teach the six phrases, out loud: **"Always…" / "Never…"** (a
   permanent rule) · **"Remember that…"** (a fact) · **"From now on…"**
   (a preference change) · **"Don't do that again"** (a correction that
   sticks) · **"When I ask for X, I mean Y"** (interpretation). Each
   changes the system permanently — talking is how they program it.
6. **The contract (→ CONTRACT.md):** read the five starter laws back in
   plain words. Then ask: "What should this system never do without
   asking you first? Anything you'd add?" New laws get written on the
   spot, in their words. (Outbound and money are already permanent.)

## ★ THE FINISH LINE

Everything below happens in one stretch — it's five minutes and it's the
best part. Do not let the owner leave before it.

1. **The context test.** "Ask me something about your business — anything
   you'd actually want to know." Answer it from what you've learned. A
   generic answer means something's missing and you say so; an answer
   that knows their business is the proof this thing is real. Never skip
   this — it's the moment the system stops being a folder.
2. **Declare it done, plainly:** "That's onboarding. Your system knows
   your business, knows you, and has its laws — it's working, right now.
   From here it just gets sharper the more you use it." Not "you've
   completed step 4 of 9." Done.
3. **Point at the workshop:** "Your setup sheet has the link to book your
   workshop — that's where the tools that need real wiring get connected
   and the first build happens." Never book it yourself; never chase it.
   Mention it once, warmly.
4. **Run the generation rules** (below).
5. **Write what's left into STATE.md**, as ordinary rows in Up next —
   not as homework, not as a debt:
   - **Connect your tools** — one row. The click-in ones (calendar,
     email, drive, and so on) can happen any time the owner has two
     minutes: they say the word, you walk them through the sign-in.
     Anything needing a key or real engineering gets its own row marked
     for the workshop. Offer the easy ones in a later session — once,
     lightly — never nag.
   - **The deeper context** — one row: writing samples so drafts sound
     like them, the 90-day priorities, and a proper walk through their
     most painful repeated work to pick the first build. Say plainly
     that these make the system noticeably better and can happen any
     time, including right now if they've got energy.
6. **Then offer, once:** "Want to keep going while we're here, or stop
   and come back?" Both answers are good ones. If they keep going, work
   the STATE rows conversationally — you don't need a script for
   "what are your priorities."

**Generation rules:**

1. Write everything captured into the knowledge/ files — owner's words,
   headed sections, nothing invented. Set each "Last confirmed" to today.
   PERSONA.md and CONTRACT.md were written live in Part 2 — read them
   back and confirm they sound like the owner.
   **No file ships raw.** Every file in knowledge/ gets opened at this
   step, including ones this conversation never reached. A file with
   nothing in it yet gets its brackets stripped, today's date, and one
   honest line — "not captured yet; it's in Up next" — so the owner never
   opens their own knowledge base and finds a fill-in-the-blank form
   staring back. An untouched template file is a broken promise, not a
   placeholder.
2. Fill STATE.md: real work into Active, the rows above into Up next.
   Delete the EXAMPLE row.
3. **The problem list:** `knowledge/problem-list.md` holds every painful
   or repeated thing named so far, in their words — nothing scored,
   nothing promised. If the file arrived pre-filled from the sales
   conversation, confirm its contents rather than rewriting them.
4. Replace [BUSINESS NAME] and [OWNER NAME] everywhere, including
   CLAUDE.md and AGENTS.md (keep both identical).
5. Scan the folder for remaining [BRACKETED] placeholders, skipping
   `_template` folders. Any left → ask.
6. Stamp the install: append to decisions.md — "Installed from Rhiza OS
   template, [date], template commit [short hash]."
7. Write `knowledge/your-map.md`, five beats: (1) welcome, one line;
   (2) talk to it — what it knows about them, and the six teach phrases;
   (3) where things live, in their actual contents, not generic labels;
   (4) your one command, /handoff; (5) what it never does, and what's
   waiting in Up next. Their register, no builder's name.
8. **Delete setup/ entirely** — this file and the sheet with it.
9. Run /handoff.

## The homework question — resolved (2026-08-08)

> There is no separate homework sheet, by design: "there is only the
> manual" (the lifecycle session's merge, RHI-34). What the owner brings
> to the workshop is produced by the finish line above — the problem
> list confirmed in their words, and the Up-next walk through their most
> painful repeated work when they have the energy. The setup sheet
> (START-HERE.md) carries the booking link and the bootstrap steps.
> Nothing else travels; nothing gets improvised.
