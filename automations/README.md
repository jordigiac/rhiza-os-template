# automations/ — what runs on its own

Each automation gets one folder here holding its record: an ABOUT.md (what it
does, where it lives, its trust status), a SETUP.md (how it was authorized and
how to verify it), and its logs — or a pointer to where logs land.

**A build's folder is born the moment it's scoped** — at a call, by a person.
The ABOUT.md holds the spec from day one; STATE.md keeps only a one-line
"Up next" row pointing here. Scoping is always a human act: the owner or
their builder starts that conversation, never this system.

Three things worth knowing:

- **The code lives next door, never in here.** When an automation genuinely
  needs a script, the script goes in the sibling folder beside this OS: one
  folder next to yours, one subfolder per automation, named to match its
  record in here (contract law 10). This folder is the map; the machinery
  sits in the building next door, and every ABOUT.md says exactly where.
  That split is what keeps this OS plain markdown that any AI can read, and
  what stops it turning into half-documentation, half-codebase as it grows.
  Scripts are reserved for automations that truly need them: prompt-only
  beats prompt-plus-script whenever language can do the job.
- **Every automation climbs a trust ladder.** It starts as a **beta**
  (a person checks every run), gets **proven** (it passes this business's
  custom quality checks consistently), and only then runs **automated**.
  Anything that sends outbound messages or moves money keeps a human yes
  forever, unless the owner explicitly decides otherwise.
- **Every automation runs on the lowest rung of the cost ladder that
  works.** (1) A pure script — no AI at runtime, near-free forever;
  intelligence gets used once, at build time. (2) Conditional — a cheap
  scripted check runs on the clock, and the AI wakes only when the check
  finds something. (3) A full agent on every run — last resort, only when
  each run truly needs judgment. This rides beside the trust ladder (one
  governs safety, the other cost) and is what keeps this OS affordable on
  a regular Claude subscription.

**A grade that makes the owner go somewhere never gets given.** If an
automation needs a quality check, it collects that check where the owner
already is — in the chat, at the close of a session — and the system writes
the answer into the record itself. The trust ladder above is unclimbable
when the evidence for climbing it lives in a file nobody opens.

Every automation here was watched running successfully before it was
installed, and each one keeps logs so its health can be checked at any time.
Logs live beside the code in the sibling folder; the ABOUT.md says where.

Copy `_template/` to start a new automation record.
