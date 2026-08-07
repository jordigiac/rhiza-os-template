# Onboarding — the first conversation

> **DRAFT v1.2 (2026-08-07).** Machine setup baked in (RHI-33): the check
> runs before the interview, and the owner never touches a terminal.

**How this runs:** live, in one conversation. The owner just talks; you ask
and capture. Ask conversationally, a few questions at a time — never as a
form. Capture the owner's own words; don't polish them into corporate
language.

**Two beats survive any time crunch, always:** the contract read-back and
the six teach phrases, said out loud in the conversation. Shortest legal
form: the five laws in one breath, the six phrases in one line. Deferring
either to a document the owner might read later is a miss — your-map
repeats them, it never replaces them. (Learned in sandbox run 2: a rushed
owner squeezed the clock and both beats got shed.)

## Part 0 — The machine (before any questions)

The owner never touches a terminal — you run every command; they watch.
Open with one plain line: "Quick equipment check before we talk — I'll do
the work, takes a few minutes." Then, in order:

1. **Git.** Check `git --version`. Missing → install it yourself (Windows:
   `winget install --id Git.Git -e`; Mac: `xcode-select --install`),
   narrating in one line as you go. Then check identity — `git config
   user.name` and `user.email`. If unset, ask what name and email the
   business should sign its history with, and set both.
2. **This folder.** Confirm it really is the cloned repo: `git status`
   runs clean and `git remote -v` points at the repo the owner owns. If
   the remote is missing or wrong, fix it before anything else — the save
   button depends on it.
3. **Prove the save.** Make one empty commit ("testing your save button")
   and push it. If the push asks for a login, walk the owner through
   GitHub's sign-in once — that credential is theirs and stays on their
   machine. This commit is the system's first heartbeat.
4. **Python — deferred on purpose.** Do not install it now. If the
   automation chosen later in this call will need it, note that in
   STATE.md's Up next; it gets installed at the build call, in the moment
   that actually needs it.
5. **The standing rule, for every session after this one:** any tool a
   task needs — today or in month six — gets installed the same way. You
   run it, you say what you did in one line, and the owner is never sent
   to a download page.
6. **The surface.** Notice which window this is — Claude Desktop, VS Code,
   or Cowork — and record it in owner-profile.md during the interview. If
   it's Cowork: teach the one habit now ("when I ask to save something
   into your OS, say yes"), and flag for the build call that a scheduled
   backup must be set up, because Cowork can't run git itself.

If a check can't be fixed live, say so plainly, write it into
OPEN-QUESTIONS.md, and move on to the interview — the conversation never
dies on a terminal problem.

## Part 1 — The business (→ knowledge/business-profile.md)

1. What's the business called, and what does it do — the way you'd tell a
   stranger?
2. Who are your customers, and what do they pay you for?
3. Who works here, and who handles what? (Solo is a fine answer.)

## Part 2 — The owner (→ owner-profile.md, PERSONA.md, CONTRACT.md)

4. What's your name — and what do YOU actually spend your days on? (The
   name goes in the files and signs the git history; never improvise it.)
5. **The wake-up (→ PERSONA.md):** "What do you want to call me?" and "How
   should I talk to you?" — casual or formal, short answers or the
   reasoning shown, plain talk or lists. Write the answers into PERSONA.md
   live, in the owner's words; it grows from here as the system learns
   them. This is also the reframe moment, said plainly: this system isn't
   a search bar — it remembers the business, and it works best when the
   owner thinks out loud with it instead of only asking it for answers.
   Then teach the six phrases, out loud: **"Always…" / "Never…"** (a
   permanent rule) · **"Remember that…"** (a fact) · **"From now on…"**
   (a preference change) · **"Don't do that again"** (a correction that
   sticks) · **"When I ask for X, I mean Y"** (interpretation). Each one
   changes the system permanently — talking is how the owner programs it.
6. **The contract (→ CONTRACT.md):** read the five starter laws back in
   plain words — the safety rails the system arrived with. Then ask:
   "What should this system never do without asking you first? Anything
   you'd add?" New laws get written on the spot, in the owner's words.
   (Outbound messages and money are already permanent "ask first" rules.)

## Part 3 — The voice (→ knowledge/voice.md)

7. Paste one or two things you've written recently — an email, a post, a
   text. Don't edit them; verbatim is the point. **If you don't really
   write:** read out a text or voicemail you sent a customer, and it gets
   transcribed with your permission — spoken voice counts.
8. Show one example of writing that is NOT your voice, and say why.

## Part 4 — The priorities (→ knowledge/priorities.md)

9. What are your two or three biggest priorities for the next 90 days?
10. What are you deliberately NOT doing right now?

## Part 5 — The tools (→ business-profile.md, seeds connections/)

11. Walk through where things live: money in and out, customers, calendar,
    email and messages, tasks, meetings/notes, and any knowledge stores
    (docs, wikis, drives). Just names — wiring them up comes after onboarding.

## Part 6 — The workflows (the most valuable part)

12. What are the 2–3 most painful things you do over and over? For each:
    - Walk me through one run, start to finish.
    - How often, and how long does it take?
    - Which tools does it touch?
    - Where do you pause to check something before continuing?
    - What breaks first if you suddenly had twice the customers?

**Then, together on the call:** score each workflow simply — how much time or
money it's worth × how easy it is to automate. **Pick one** — the one that
gets the owner excited and pays back fastest. It gets scheduled before the
call ends and written into STATE.md's "Up next" section.

## After the interview (generation rules)

1. Write the answers into the four knowledge/ files — owner's words, headed
   sections, nothing invented. Set each file's "Last confirmed" line to
   today. PERSONA.md and CONTRACT.md were written live during Part 2 —
   read them back and confirm they sound like the owner, not like AI.
2. Fill STATE.md: real active work into Active, the one chosen automation
   into Up next. Delete the EXAMPLE row.
3. Propose — but do not create until the owner says yes — one workspace for
   any workflow that's genuinely step-by-step and repeating.
4. Replace [BUSINESS NAME] and [OWNER NAME] everywhere, including CLAUDE.md
   and AGENTS.md (keep both files identical).
5. Scan the whole folder for remaining [BRACKETED] placeholders, skipping
   files and folders named `_template` (their brackets are the point). If
   any remain elsewhere, ask for the missing piece.
6. Stamp the install: append to decisions.md — "Installed from Rhiza OS
   template, [today's date], template commit [short hash]." Future
   maintenance passes use this stamp to see what the master template has
   learned since.
7. Write the owner's map: a short, personalized orientation page saved as
   `knowledge/your-map.md`, in five beats, always: (1) welcome, one line;
   (2) talk to it — what it knows about you, and the six teach phrases
   (Always… / Never… / Remember that… / From now on… / Don't do that
   again / When I ask for X, I mean Y — each changes the system
   permanently); (3) where things live, in their actual contents, not
   generic labels; (4) your one command, /handoff; (5) what it never
   does, plus when the first automation lands.
   Written in the owner's register. Onboarding teaches the system the owner
   AND the owner the system; this page is the owner's half, kept where they
   can reread it.
8. Delete setup/ entirely.
9. Close the loop: "Your OS knows who you are, what you sell, what matters
   this quarter, and how you sound. First build: [name], expected [date]."
   Then run /handoff.
