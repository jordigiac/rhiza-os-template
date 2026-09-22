# Onboarding — the first conversation

> **v4.0, async with a real finish line.** The owner does this alone, at
> their own pace, with nobody on the other end. The standard: a
> non-technical person on a fresh machine, either platform, finishes
> without help.

**The shape, and why it matters.** Onboarding is **context**: teaching the
system the business. It finishes at the line marked ★ below, and when it
finishes it is *done*, not paused. Everything after that line, connecting
tools and the deeper questions, is ordinary work in a working system,
tracked in STATE.md like anything else. There is no such thing as an
abandoned onboarding here. There is "not finished yet" before the line and
"using it" after.

**How this runs:** conversational and self-paced. The owner talks; you ask
and capture, a few questions at a time, never a form. Keep their own words.
If they vanish mid-sentence, nothing is lost.

**Two beats survive any time crunch:** the contract read-back and the six
teach phrases, said out loud. Shortest legal form: the laws in one breath,
six phrases in one line. Never deferred to a document.

**Never name the person who built this.** The system belongs to the owner
alone. If they're stuck on something technical, point at "the setup sheet
you followed, it has contact details." That sheet is the only place a
builder's name appears, and it deletes with this file.

## Progress — tick as parts complete; this block IS the resume state

- [ ] Part 0 — the machine
- [ ] Part 1 — the business (the core)
- [ ] Part 2 — the owner, the voice, the persona, the contract
- [ ] ★ THE FINISH LINE — context test · completion declared · files written

**Resuming:** while this folder exists, onboarding is unfinished. Any
session starting here reads this block, greets the owner back warmly,
"picking up where we left off, you were telling me about X," and continues.
Never restart a finished part. Never make them repeat themselves.

**A tick means it's written.** Never tick a box for something that only
happened in conversation. The box is a claim about what's on disk, and the
next session believes it completely.

## Part 0 — The machine (before any questions)

The owner never touches a terminal. You run every command; they watch.
Detect the platform first, Windows or Mac, and use only its commands. Open
with one plain line: "Quick equipment check before we talk. I'll do the
work, takes a few minutes." Then:

1. **Their own copy.** Before anything else, confirm this folder is a repo
   *they* own and can push to. If they used **Use this template** on GitHub
   and cloned that, they're fine. If they cloned the public template
   directly, they cannot save, and every backup from here on would fail
   silently. Fix it now: have them make their own private copy on GitHub,
   then point this folder at it. The setup sheet has the steps.
2. **Git.** Check `git --version`. Missing means install it yourself
   (Windows: `winget install --id Git.Git -e`; Mac: `xcode-select
   --install`), narrating in one line. Then check identity, `git config
   user.name` and `user.email`. If unset, or set to someone who isn't the
   owner, ask what name and email the business should sign its history
   with, and set both.
3. **This folder.** `git status` clean, `git remote -v` pointing at the
   repo from step 1.
4. **Prove the save.** One empty commit ("testing your save button"),
   pushed. If it asks for a login, walk them through it once. That
   credential is theirs and stays on their machine. This is the system's
   first heartbeat, and everything after it assumes it worked.
5. **Install the hourly backup.** Open `automations/os-autosave/SETUP.md`,
   run the one command for their platform with their folder path, and
   confirm the scheduled job exists. Tell them plainly what it does: every
   hour, this folder saves itself to their GitHub, so nothing lives only on
   this laptop. It never writes a file and never sends anything.
6. **Python, deferred on purpose.** Don't install it now. If a later build
   needs it, it gets installed then.
7. **The standing rule, forever after:** any tool a task needs gets
   installed the same way. You run it, you say what you did in one line,
   and the owner is never sent to a download page.
8. **The surface.** Note which window this is, VS Code or the Claude
   desktop app, and **write it into owner-profile.md immediately, not
   later**. Part 0 isn't ticked until that line exists on disk. If this
   surface can't run git itself, say so plainly and confirm the hourly
   backup from step 5 is installed, because that becomes the only save.

If a check can't be fixed: say so plainly, point at the setup sheet's
contact line, write it into OPEN-QUESTIONS.md, and carry on. The
conversation never dies on a terminal problem.

## Part 1 — The business (→ knowledge/core/)

These answers become the core: the files every draft this system ever makes
gets built from. Take them slowly, and read names back before writing them.

**Say this first, once:** "These next answers become the part of your system
I check before I write anything for you. They only change when you tell me
to, so it's worth getting them right."

1. **What's the business called, and what does it do, the way you'd tell a
   stranger?** Spell the name back. A mangled business name gets caught
   here or it lives in files forever. → `core/business-profile.md`
2. **Why does it exist? What are you actually trying to do for people?**
   → `core/business-profile.md`
3. **Who do you serve?** Not a market segment; the actual person. What are
   they trying to do, what's in the way, and what do they say when they
   describe it? Capture their phrases word for word if the owner quotes
   any. → `core/audience.md`
4. **Walk me through everything you sell.** One at a time: what it is, what
   it costs, how it's delivered, where the sales page lives, whether it's
   open right now, and when it runs next. Include the free things: the lead
   magnet, the challenge, the free training, and what each leads into.
   → `core/offers.md`
5. **Who works with you, and who handles what?** Contractors count: the VA,
   the editor, the launch manager. Solo is a fine answer in one line.
   → `core/team-and-tools.md`
6. **Which tools does the business actually run on?** Walk the list out
   loud: email list, calendar and booking, live sessions, payments and
   invoicing, where clients and leads live, files, website, course
   platform, social. Fill the table. **Then make a stub in `connections/`
   for each one named**, saying what it is and that it isn't wired yet.
   That's what makes "connect my calendar" a two-minute job later instead
   of a conversation from scratch. → `core/team-and-tools.md` + `connections/`
7. **Do you do joint ventures, affiliate promos, or swaps with other
   people's audiences?** If yes: who, roughly how big their list is, what
   you've done together, and what they need from you when you launch. One
   file each in `knowledge/partners/`. If no, say so in one line and move on.
8. **Your clients: do you want a roster in one file, or a file each?**
   Either is fine. Start the shape they pick in `knowledge/clients/`.

## Part 2 — The owner, the voice, and the laws

9. **What's your name, and what do you actually spend your days on?** The
   name goes in the files and signs the git history. Never improvise it.
   → `knowledge/owner-profile.md`

10. **The voice bank.** "Paste me three to five things you've actually
    written. A launch email, a post, a sales page, a long DM. Whatever's
    easiest to find." Paste them into `core/voice-samples.md` exactly as
    written, typos included, each labelled with what it was and who read
    it. Then read them and draft `core/voice.md`: how they open, sentence
    length, contractions, punctuation habits, the words they reach for, how
    they close. Read that description back and let them correct it.

    Say why, in one line: "This is how I'll sound when I write as you. When
    you rewrite something of mine later, I'll ask to keep your version,
    because your edit teaches me more than anything else."

11. **The wake-up (→ PERSONA.md).** "What do you want to call me?" and "How
    should I talk to you?" Show them the defaults already in PERSONA.md and
    let them change any of it. Write it live, in their words.

    Two more questions while you're here:
    - **"When you think out loud at me, do you want your words kept exactly
      as you said them, or cleaned up so they're clearer later?"** Their
      answer goes into PERSONA.md under how they like their words handled
      (contract law 3).
    - **"Do you want one main focus named at a time on your board, or do
      you prefer to see everything at once?"** Their answer shapes STATE.md.

    This is also the reframe, said plainly: this system isn't a search bar.
    It remembers the business, and it works best when you think out loud
    with it instead of only asking it questions.

    Then teach the six phrases, out loud: **"Always…" / "Never…"** (a
    permanent rule) · **"Remember that…"** (a fact) · **"From now on…"** (a
    preference change) · **"Don't do that again"** (a correction that
    sticks) · **"When I ask for X, I mean Y"** (interpretation). Each one
    changes the system permanently. Talking is how they program it.

12. **The contract (→ CONTRACT.md).** Read the laws back in plain words,
    quickly. The ones worth landing: nothing goes out and no money moves
    without your yes; your core facts change only when you say so; I'll
    tell you what I'm doing while I do it; pivots are fine and I'll never
    guilt you about one. Then ask: "What should this system never do
    without asking you first? Anything you'd add?" New laws get written on
    the spot, in their words.

## ★ THE FINISH LINE

Everything below happens in one stretch. It's five minutes and it's the
best part. Do not let the owner leave before it.

1. **The context test.** "Ask me something about your business, anything
   you'd actually want to know." Answer it from what you've learned. A
   generic answer means something's missing and you say so. An answer that
   knows their business is the proof this thing is real. Never skip this.
   It's the moment the system stops being a folder.
2. **Declare it done, plainly:** "That's onboarding. Your system knows your
   business, knows you, and has its laws. It's working, right now. From
   here it just gets sharper the more you use it." Not "you've completed
   step 4 of 9." Done.
3. **Start their first piece of real work.** "What's the next thing you're
   launching or running, and when?" Make
   `workspaces/launches/<name>/CONTEXT.md` with what they just said: the
   offer, the date, who's involved, what has to go out. If nothing is
   coming up, skip it without ceremony. Seeing one real piece of work in
   the folder is what makes the rest make sense.
4. **Mention the help, once, warmly.** "If you'd rather not build the rest
   of this alone, the setup sheet has a link to get it done with you on two
   short calls." Never book anything. Never chase. Say it once.
5. **Run the generation rules** (below).
6. **Write what's left into STATE.md**, as ordinary rows in Up next, not as
   homework and not as a debt:
   - **Connect your tools** — one row. The click-in ones can happen any
     time the owner has two minutes: they say the word, you walk them
     through the sign-in. Anything needing a key gets its own row. Offer
     the easy ones in a later session, once, lightly. Never nag.
   - **The deeper context** — one row: the 90-day priorities, and a proper
     walk through their most painful repeated work to pick the first build.
     Say plainly that these make the system noticeably better and can
     happen any time, including right now if they've got energy.
7. **Then offer, once:** "Want to keep going while we're here, or stop and
   come back?" Both answers are good ones. If they keep going, work the
   STATE rows conversationally. You don't need a script for "what are your
   priorities."

**Generation rules:**

1. Write everything captured into the knowledge/ files, in the owner's
   words, headed sections, nothing invented. Set each "Last confirmed" to
   today.
   **No file ships raw.** Every file in knowledge/ gets opened at this step,
   including ones this conversation never reached. A file with nothing in it
   yet gets its brackets stripped, today's date, and one honest line, "not
   captured yet; it's in Up next," so the owner never opens their own
   knowledge base and finds a fill-in-the-blank form staring back. An
   untouched template file is a broken promise, not a placeholder.
2. PERSONA.md and CONTRACT.md were written live in Part 2. Read them back
   and confirm they sound like the owner.
3. Fill STATE.md: real work into Active, the rows above into Up next.
   Delete the EXAMPLE row.
4. **The problem list.** `knowledge/problem-list.md` holds every painful or
   repeated thing named so far, in their words. Nothing scored, nothing
   promised.
5. Replace [BUSINESS NAME] and [OWNER NAME] everywhere, including CLAUDE.md
   and AGENTS.md. Keep those two identical.
6. Scan the folder for remaining [BRACKETED] placeholders, skipping
   `_template` folders. Any left means ask.
7. Stamp the install: append to decisions.md, "Installed from the Rhiza OS
   template, [date], template version [the release name or date shown in
   the repo]."
8. Write `knowledge/your-map.md`, five beats: (1) welcome, one line; (2)
   talk to it — what it knows about them, and the six teach phrases; (3)
   where things live, in their actual contents, not generic labels, and
   what makes `core/` different; (4) the handful of things that are theirs
   to say: say hey to open, tell it you're done to close and save, ask for
   a checkup when its facts feel stale, ask for an audit once a month; (5)
   what it never does, and what's waiting in Up next. Their register, no
   builder's name.
9. **Delete setup/ entirely**, this file and the sheet with it.
10. **Move the owner home (the bootstrap case).** If this conversation
    started outside the system's folder, because the owner opened Documents
    and pasted the setup line, run `code <the system's folder>` so VS Code
    opens it in its own window, and say plainly: "One last thing: a new
    window just opened on your system's folder. That window is home now.
    Talk to me there from today on, and VS Code will remember it." Without
    this, tomorrow's "hey" lands in Documents, where the system can't hear
    them.
11. Run the handoff skill.
