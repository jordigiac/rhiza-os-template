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

**The quality bar, during this one conversation.** Everything this system
writes normally runs the Gate in `evals/` before a person sees it. Onboarding
is the exception that proves it, because the owner is in the room saying every
word. So the rule here is narrower and stricter: **write only what they said.**
Read back anything exact before it lands, especially prices, dates and links.
Anything you inferred gets marked as yours and asked about. Nothing in
`knowledge/core/` may be a guess. From the moment `setup/` is deleted, the
normal bar applies to everything.

**Never name the person who built this** during the conversation. The system
belongs to the owner alone. If they're stuck on something technical, point at
"the setup sheet you followed, it has contact details." That sheet deletes
with this file, and generation rule 7 clears the last of it out of the README.

**When the owner's answer contradicts something that shipped in this
template, the owner wins.** It will happen, probably more than once: a
default in PERSONA.md, a line in a README, a rule they want stricter than
ours. Change the shipped file to match them, say in one line that you did,
and log it in decisions.md as their call. Never argue the template's side,
and never quietly keep both.

## Progress — tick as parts complete; this block IS the resume state

- [ ] Part 0 — the machine
- [ ] Part 1 — the business (the core)
- [ ] Part 2 — the owner, the voice, the persona, the contract
- [ ] ★ Finish line 1 — the context test
- [ ] ★ Finish line 2 — completion declared, first workspace started
- [ ] ★ Finish line 3 — the generation rules, all of them, files written

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
   *they* own and can push to. If they cloned the public template directly,
   they cannot save, and every backup from here on would fail silently.

   The check, in order:
   - `git remote -v`. If the URL is the public template's, that is the
     problem, and say so plainly.
   - `git push --dry-run`. Permission denied means the same thing.

   The fix, which you walk them through: on GitHub, open the template and
   click **Use this template → Create a new repository**, private, named
   after their business. Copy its URL. Then here:
   `git remote set-url origin <their new URL>` and push for real. Now they
   own it.
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
5. **Install the hourly backup.** Open `automations/os-autosave/SETUP.md`
   and run the block for their platform with their folder path. Then
   **prove it, in the same minute**: run the job by hand as that file
   describes, and confirm a commit called `autosave` actually landed on
   their GitHub. The job existing is not the test. The commit is the test.

   Tell them plainly what it does: every hour, this folder saves itself to
   their GitHub, so nothing lives only on this laptop. It never writes a
   file and never sends anything.

   **If the commit does not land, say so and do not tick this box.** Write
   it into OPEN-QUESTIONS.md and add a STATE.md row, then tell them in one
   line: "your hourly backup isn't running yet, so closing properly is your
   only save until we fix it." A backup believed in is worse than no backup
   at all.
6. **Python, deferred on purpose.** Don't install it now. If a later build
   needs it, it gets installed then.
7. **The standing rule, forever after:** any tool a task needs gets
   installed the same way. You run it, you say what you did in one line,
   and the owner is never sent to a download page.
8. **The surface.** Note which window this actually is, whatever it is:
   VS Code with Claude Code, the Claude desktop app, a terminal, something
   else. Write it into owner-profile.md in plain words, **immediately, not
   later**. Part 0 isn't ticked until that line exists on disk. If this
   surface can't run git itself, say so plainly and make sure the hourly
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

   **Every date gets a year and every time gets a zone, out loud, read
   back.** "October 14" is not a date, it is two dates. This file exists so
   a wrong date never reaches a customer, and a date without a year is how
   that happens. Ask for their time zone once here and write it into
   `core/business-profile.md` too, because the system schedules against
   it.
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
   Either is fine. If they pick a roster, make `clients/roster.md` with the
   headings and any names they give you. If they pick a file each, don't
   create empty files: write one line in `clients/README.md` saying that's
   the shape, and make the first real file the next time they mention a
   client by name.

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

   *If the owner has gone quiet and can't ask, don't fake it and don't tick
   the box. Ask yourself one hard question about their business instead,
   answer it, write both into OPEN-QUESTIONS.md as "context test still
   owed," and put it first in the next session.*
2. **Declare it done, plainly:** "That's onboarding. Your system knows your
   business, knows you, and has its laws. It's working, right now. From
   here it just gets sharper the more you use it." Not "you've completed
   step 4 of 9." Done.
3. **Start their first piece of real work.** "What's the next thing you're
   launching or running, and when?" Copy `workspaces/_template/RUN.md` to
   `workspaces/launches/<name>/RUN.md` and fill what they just said: the
   offer, the dates with their years, who's involved, the links, what has
   to go out. Leave the rest as open questions. If nothing is coming up,
   skip it without ceremony. Seeing one real piece of work in the folder is
   what makes the rest make sense.
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
5. Replace [BUSINESS NAME] and [OWNER NAME] everywhere, including
   CLAUDE.md, AGENTS.md and CONTRACT.md's first line. Keep CLAUDE.md and
   AGENTS.md identical.
6. Check for leftover blanks. Read every file in `knowledge/` and
   `connections/`, plus CLAUDE.md, AGENTS.md, CONTRACT.md, PERSONA.md,
   STATE.md and README.md, and look for
   square-bracket prompts that are still instructions to fill something in.
   Skip `_template` folders, skip `.claude/`, and ignore ordinary markdown
   links, which also use square brackets. Anything genuinely unfilled means
   ask, or write the honest "not captured yet" line from rule 1.
7. **Rewrite README.md as theirs.** The one that shipped is the template's
   shop window: it sells a setup service, links to the `setup/` folder
   about to be deleted, and names the people who built this. None of that
   belongs in their business's repo. Replace it with a short one, in their
   register: what this folder is, what's in it, and how they talk to it.
   Keep one line of credit for where the template came from if they want
   it; ask.
8. Stamp the install: read the `VERSION` file at the top of this folder
   and append to decisions.md, "Installed from the Rhiza OS template,
   [date], template version [the version line from VERSION]." Then delete
   `VERSION`. It described the starting kit; from here the history is this
   business's own.
9. Write `knowledge/your-map.md`, five beats: (1) welcome, one line; (2)
   talk to it — what it knows about them, and the six teach phrases; (3)
   where things live, in their actual contents, not generic labels, and
   what makes `core/` different; (4) the handful of things that are theirs
   to say: say hey to open, tell it you're done to close and save, ask for
   a checkup when its facts feel stale, ask for an audit once a month; (5)
   what it never does, and what's waiting in Up next. Their register, no
   builder's name.
10. **Delete setup/ entirely**, this file and the sheet with it.
11. **Move the owner home (the bootstrap case).** If this conversation
    started outside the system's folder, because the owner opened Documents
    and pasted the setup line, they need to end up *in* the folder or
    tomorrow's "hey" lands in Documents where the system can't hear them.
    Try `code <the system's folder>`. If that command isn't found, which is
    normal on a fresh machine and always true in the desktop app, don't
    retry it. Tell them in one line what to click instead: "Open your
    business folder in this app from now on, it's the one in Documents
    called <name>. Everything we just did is in there." Then confirm they
    can see it before you finish.
12. Run the handoff skill, which saves all of this.
