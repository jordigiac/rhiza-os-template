# automations/ — what runs on its own

Each automation gets one folder here holding its record: an ABOUT.md (what it
does, where it lives, its trust status), a SETUP.md (how it was authorized and
how to verify it), and its logs — or a pointer to where logs land.

**A build's folder is born the moment it's scoped** — at a call, by a person.
The ABOUT.md holds the spec from day one; STATE.md keeps only a one-line
"Up next" row pointing here. Scoping is always a human act: the owner or
their builder starts that conversation, never this system.

Three things worth knowing:

- **The code may live elsewhere.** Bigger automations that run in the cloud
  get their own small, clearly-labeled repo so runs stay fast and lean. The
  ABOUT.md always says where. This folder is the map; the machinery can sit
  in another building. Scripts are reserved for automations that genuinely
  need them — prompt-only beats prompt-plus-script whenever language can do
  the job.
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

Every automation here was watched running successfully before it was
installed, and each one keeps logs so its health can be checked at any time.

Copy `_template/` to start a new automation record.
