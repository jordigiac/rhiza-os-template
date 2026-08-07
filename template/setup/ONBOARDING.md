# Onboarding — the first conversation

> **v2.0 (2026-08-07), async-first.** The owner completes this entirely
> alone, at their own pace, across as many sittings as they need — nobody
> is on the other end. The standard: a random non-technical person on a
> fresh machine, either platform, finishes this without help.

**How this runs:** conversational and self-paced. The owner just talks; you
ask and capture, a few questions at a time — never a form. Capture the
owner's own words; don't polish them into corporate language. If the owner
disappears mid-sentence, nothing is lost — see Resuming.

**Two beats survive any time crunch, always:** the contract read-back and
the six teach phrases, said out loud in the conversation. Shortest legal
form: the five laws in one breath, the six phrases in one line. Deferring
either to a document the owner might read later is a miss — your-map
repeats them, it never replaces them.

**If anything can't be fixed or gets confusing:** say so plainly and point
at the builder — [BUILDER NAME], [BUILDER CONTACT], replies same-day on
weekdays. A stalled install never dead-ends. Then keep going with whatever
can continue.

## Progress — tick as parts complete; this block IS the resume state

- [ ] Part 0 — the machine
- [ ] Part 1 — the business
- [ ] Part 2 — the owner, the persona, the contract
- [ ] ★ Minimum viable install reached (declared out loud)
- [ ] Part 3 — the voice
- [ ] Part 4 — the priorities
- [ ] Part 5 — the tools, names only
- [ ] Part 5½ — connections (OAuth only, calendar first)
- [ ] [SLOT] homework sheets
- [ ] Part 6 — the workflows, one build picked
- [ ] The close — context test · booking offer · generation rules

**Resuming:** while this folder exists, onboarding is in progress. Any
session that starts here reads this block, greets the owner back warmly —
"picking up where we left off, you were telling me about X" — and
continues. Never restart a finished part; never make the owner repeat
themselves.

## Part 0 — The machine (before any questions)

The owner never touches a terminal — you run every command; they watch.
Detect the platform first (Windows or Mac) and use only its commands —
never show the owner the other platform's noise. Open with one plain line:
"Quick equipment check before we talk — I'll do the work, takes a few
minutes." Then, in order:

1. **Git.** Check `git --version`. Missing → install it yourself (Windows:
   `winget install --id Git.Git -e`; Mac: `xcode-select --install`),
   narrating in one line as you go. Then check identity — `git config
   user.name` and `user.email`. If unset — or set to someone who isn't the
   owner — ask what name and email the business should sign its history
   with, and set both.
2. **This folder.** Confirm it really is the cloned repo: `git status`
   runs clean and `git remote -v` points at the repo the owner owns. If
   the remote is missing or wrong, fix it before anything else — the save
   button depends on it.
3. **Prove the save.** Make one empty commit ("testing your save button")
   and push it. If the push asks for a login, walk the owner through
   GitHub's sign-in once — that credential is theirs and stays on their
   machine. This commit is the system's first heartbeat.
4. **Python — deferred on purpose.** Do not install it now. If the
   build chosen later will need it, note that in STATE.md's Up next; it
   gets installed at the working call, in the moment that needs it.
5. **The standing rule, for every session after this one:** any tool a
   task needs — today or in month six — gets installed the same way. You
   run it, you say what you did in one line, and the owner is never sent
   to a download page.
6. **The surface.** Notice which window this is — Claude Desktop, VS Code,
   or Cowork — and record it in owner-profile.md during the interview. If
   it's Cowork: teach the one habit now ("when I ask to save something
   into your OS, say yes"), and flag for the working call that a scheduled
   backup must be set up, because Cowork can't run git itself.

If a check can't be fixed live: the escape hatch above, then continue with
the interview — the conversation never dies on a terminal problem.

## Part 1 — The business (→ knowledge/business-profile.md)

1. What's the business called, and what does it do — the way you'd tell a
   stranger? (Names get spell-checked out loud: a mangled or inconsistent
   business name gets caught and confirmed, never silently filed.)
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

**★ Minimum viable install — declare it out loud:** "From here, your
system works. It knows the business, it knows you, and it has its laws.
Everything after this makes it sharper. Stop anytime — I'll pick you right
back up." Tick the Progress box.

## Part 3 — The voice (→ knowledge/voice.md)

7. Paste one or two things you've written recently — an email, a post, a
   text. Don't edit them; verbatim is the point. **If they don't really
   write:** their messages in THIS conversation are already a sample —
   quote their own lines back, name the patterns, and confirm that's the
   real voice. (A voicemail or text read out loud works too.)
8. Show one example of writing that is NOT your voice, and say why.

## Part 4 — The priorities (→ knowledge/priorities.md)

9. What are your two or three biggest priorities for the next 90 days?
10. What are you deliberately NOT doing right now?

## Part 5 — The tools (→ business-profile.md, seeds connections/)

11. Walk through where things live: money in and out, customers, calendar,
    email and messages, tasks, meetings/notes, and any knowledge stores.
    Just names — wiring comes next.

## Part 5½ — Connections (OAuth only — calendar first, always)

Now wire the click-in connectors, together, click by click. **OAuth only:
the owner signs in; no keys, no secrets, nothing pasted — ever, in this
part.**

- **Calendar first, always** — it's how the working call gets booked from
  inside the OS at the close.
- Then whichever native Claude connectors match the tools they just named
  (email, drive, Notion, and so on). Narrate every click plainly:
  settings, connectors, sign in, done. Confirm each one works with one
  tiny real read ("your next three calendar events are…").
- **Say the deferral out loud, so nothing feels missing:** "Some of your
  tools need real engineering to connect — those are deliberately saved
  for your working call, live with [BUILDER NAME], in the first twenty
  minutes. You're not missing a step."
- For each deferred tool: create its stub file in connections/ — the
  name, what it will do, and "wired at the working call." Nothing else.

## [SLOT — homework sheets]

> **Marked slot, content pending (RHI-34):** the owner arrives at the
> working call with homework — the delegation wishlist, drawn from the
> problems captured at the sales call. The sheets' design is coming from
> the lifecycle work; when it lands, it runs here, after connections.
> Until then: skip this slot silently. Do not improvise it.

## Part 6 — The workflows (the most valuable part)

12. What are the 2–3 most painful things you do over and over? For each:
    - Walk me through one run, start to finish.
    - How often, and how long does it take?
    - Which tools does it touch?
    - Where do you pause to check something before continuing?
    - What breaks first if you suddenly had twice the customers?

**Then, together:** score each workflow simply — how much time or money
it's worth × how easy it is to automate. **Pick one** — the one that gets
the owner excited and pays back fastest. It gets written into STATE.md's
"Up next" section, to be built at the working call.

## The close (in order)

1. **The context test.** "Ask me something about your business — anything
   you'd actually want to know." A generic answer means onboarding isn't
   done; an answer that knows their business is the proof moment. This is
   the immediate-value beat — never skip it.
2. **The booking — offered, never required.** The calendar is connected,
   so offer it: "Want to book your working call right now, from in here?
   That's where [BUILDER NAME] reviews everything this conversation built
   and the first build happens live." If they'd rather not yet: "book
   later by just asking me," and the contact line stands. Warm either way.
3. **Generation rules:**
   1. Write the answers into the four knowledge/ files — owner's words,
      headed sections, nothing invented. Set each "Last confirmed" line
      to today. PERSONA.md and CONTRACT.md were written live during
      Part 2 — read them back and confirm they sound like the owner.
   2. Fill STATE.md: real active work into Active, the one chosen build
      into Up next. Delete the EXAMPLE row.
   3. Propose — but do not create until the owner says yes — one
      workspace for any workflow that's genuinely step-by-step.
   4. **The problem list has a named home:** `knowledge/problem-list.md`
      — the problems captured at the sales call land there (mechanism
      pending from the lifecycle work; if the file was delivered
      pre-filled, confirm its contents with the owner during Part 6).
   5. Replace [BUSINESS NAME], [OWNER NAME], [BUILDER NAME], and
      [BUILDER CONTACT] everywhere, including CLAUDE.md and AGENTS.md
      (keep both identical).
   6. Scan the whole folder for remaining [BRACKETED] placeholders,
      skipping `_template` folders. Any remaining → ask.
   7. Stamp the install: append to decisions.md — "Installed from Rhiza
      OS template, [date], template commit [short hash]." Maintenance
      passes read this stamp.
   8. Write the owner's map, `knowledge/your-map.md`, five beats always:
      (1) welcome, one line; (2) talk to it — what it knows, and the six
      teach phrases; (3) where things live, in their actual contents;
      (4) your one command, /handoff; (5) what it never does, when the
      working call is (or how to book it by asking), and [BUILDER NAME]'s
      contact line. Written in the owner's register.
   9. Delete setup/ entirely — this file and START-HERE with it.
   10. Close the loop: "Your OS knows who you are, what you sell, what
       matters this quarter, and how you sound. First build: [name], at
       your working call." Then run /handoff.
