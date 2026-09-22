---
name: audit
description: The OS's health check and growth scan. Measures read-only, scores the Four C's, and writes a dated report into audits/ — then offers the fix list and repairs what gets approved, right there. Growth (new skills, automations, cuts) is recommended with evidence, never built by this skill. Use for /audit or "how is the system doing". Never audits the computer itself.
---

# Audit — is this OS still telling the truth, and where can it grow?

Three acts: **measure, report, fix.** Measuring is read-only, by oath —
nothing gets fixed, renamed, moved, or deleted while the audit is looking,
because a check that edits what it's measuring is grading its own homework.
Then the report, findings and score final. Then the offer (2026-08-08):
the fix list goes to whoever ran the audit, and what they approve gets
fixed on the spot. This skill never fixes *silently*; it fixes on a yes.

Owner and builder run the same skill — whoever runs it is the one who says
yes. The report is built to be worked top to bottom: every finding pairs
with what to do about it, so the fix pass — today's or any later one —
can go down the line.

## Steps

1. Read the previous report in audits/ (if any) so the new one can show
   what changed — including which of its fixes got done.
2. Run the three passes below, collecting findings.
3. Run the growth scan.
4. Write the report to `audits/YYYY-MM-DD-audit.md` in the format at the
   bottom. Findings and scores are final once written.
5. Offer the fix list — all, some, or none — and execute what gets a yes,
   under the fixing rules below. Recommendations are noted, never executed.

## Pass 1 — health (does the structure tell the truth?)

- Routing check: every path in CLAUDE.md's map and routing table exists on
  disk, and everything on disk is reachable from the front desk. Check both
  directions. Plumbing does not need a room: skip dot-prefixed files and
  folders (.claude, .env.example, .gitignore) and AGENTS.md when checking
  reachability. Confirm AGENTS.md is identical to CLAUDE.md.
- New-hire test: open the folder cold. Can a stranger orient and route to
  any task in three reads or fewer? Name where they would get lost.
- Truth check: files untouched 30+ days that claim to be current,
  contradictions between files, the same fact written in two places,
  leftover [BRACKETED] placeholders. Files and folders named `_template`
  keep their brackets by design; skip them.
- Budget check on the always-loaded set (CLAUDE.md, AGENTS.md,
  CONTRACT.md, PERSONA.md, STATE.md): no single file over 200 lines, and
  the set under 600 together. These get read at the start of every
  session, so every line in them is a tax on every conversation. Flag any
  knowledge file that has grown crowded, and any workspace contract over
  80 lines.
- Contradiction sweep on the facts that change most: prices, offer names
  and dates, who does what, client and partner status. Read
  `knowledge/core/` against the working files and against recent
  decisions. **A core file contradicted by a working file is the finding
  that matters most** — it means drafts have been built on something
  stale. Report it; never fix core here (contract law 9).
- Dead-rule scan: a law in CONTRACT.md or a line in PERSONA.md that
  nothing has exercised in months. Flag it as a question, not a cut.

## Pass 2 — machinery (does everything still run?)

- Each automation (skip `_template` folders; those are blank starters):
  ABOUT.md matches reality (schedule, location, ladder status), logs show
  clean runs since the last report, SETUP.md's verification step still
  passes as described.
- **The backup's heartbeat:** read the date of the most recent commit. If
  the hourly backup is installed and the newest commit is more than a day
  old, the scheduled job has died quietly. That is a finding, not a note —
  it means the system has stopped saving itself.
- Each skill: present, listed in the skills README, and actually referenced
  or used. Flag anything unused or broken. Skills hygiene: critical rules
  sit above the fold in each SKILL.md (compaction truncates from the
  bottom), and no skill file has grown past roughly 5,000 words.
- Connections: each reference file names a real .env key in .env.example
  terms, and describes limits that still match how it is used.

## Pass 3 — evolution (does the system still fit the business?)

- Knowledge fresh: each fact file's "Last confirmed" age, and the claims
  themselves checked against decisions.md, STATE.md, and recent session
  evidence — contradictions become proposed corrections in this report.
  Oldest confirmation past ~45 days → flag: checkup due.
- Knowledge sized right: files that should split into a folder with an
  index, or folders that shrank back to a file.
- Workspaces still earn their place: is the work still repeating?
- STATE.md's Up next is current, with dates the owner can trust.
- `evals/correction-ledger.md`: sightings that have waited about 30 days
  without a second occurrence get proposed for retirement. A pattern that
  never came back was noise.

## The growth scan — recommended to the owner, never built here

This section is written to the owner: their system collected the evidence,
and what to do with it is their call. (The operator-only wall came down
2026-08-08 — the report hides nothing from the person it's about.)

Scan the system's own record — the journal, STATE.md history, decisions.md,
run logs, and handoff commits — for three patterns:

- **Repetition** — the same work done by hand, session after session.
  Recommend it get a named home first, manual-first: a runbook file for
  plain steps, a staged workspace where material accumulates — the
  smallest shape that fits. A manual workflow that has worn a groove is
  what graduates, later and deliberately, into a skill or an automation.
- **Proven load** — a capability run steadily and cleanly, a log showing
  growing volume: a candidate for promotion up the ladder.
- **Dead weight** — skills never invoked, connections never used,
  structure the work outgrew. Recommend the cut, explicitly.

Every recommendation carries its evidence, counted ("done by hand 6 times
since the last report"), and a suggested first step. Suggest nothing the
evidence doesn't support.

**The line that keeps this lane safe:** recommendations are recorded,
never executed — not even on an enthusiastic "fix everything." New things
get born in their own conversation, at the owner's pace, manual first, up
the trust ladder. The audit is the evidence engine, not the builder.

## Fixing — after the report, on a yes

- Read the fix list back and ask what to fix: all, some, or none.
- Weight labels say what each fix is, never who should do it — nothing is
  gated. **(quick)**: a stale line, a wording fix, an index entry.
  **(plumbing)**: code, automations, anything that runs.
- An ambiguous fix — two reasonable readings, or it touches something the
  owner might mean differently — consults before executing. Ask, not guess.
- A cut is a boxing: into archive/ per its INDEX, indexed and findable.
  This skill deletes nothing, ever.
- Each executed fix ticks its checkbox in the report, dated. The tick is
  the only edit a past report ever receives — findings, scores, and prose
  stay exactly as written.
- The score predates the fixes on purpose: this report shows the honest
  before; the improvement shows up in the next one.

## Scoring anchors — Four C's, 25 points each

**The zero line: the stock template scores zero.** Preset skills, READMEs,
blank _template files, and empty folders ship with every install — they are
the floor you measure from, never points. Score only what exists for THIS
business on top of that floor. For each C: 0–8 barely above the floor,
9–17 real but thin or unused, 18–25 current, specific, and used since the
last report.

- Context: the owner's actual facts, filled at onboarding and kept current.
  The only category an install day can raise.
- Connections: tools genuinely wired — a connection file naming a real key
  that works. The README and _template are the floor: 0.
- Capabilities: custom skills and workspaces built for this business and
  actually used. The skills that ship with the template are the floor: 0,
  in every install, always.
- Cadence: things that actually run on their own. Nothing scheduled = 0.

Sanity check before writing the score: an onboarded but unwired install is
Context in the teens or low 20s and **0 / 0 / 0** elsewhere — total ≤ 25.
If you scored an unwired install above that, you graded the box, not the
business. Start over.

## Report format

```
# Audit — YYYY-MM-DD

Four C's: NN/100 (Context NN/25, Connections NN/25, Capabilities NN/25,
Cadence NN/25). Last month: NN. One-line verdict.

## Pass 1 — health
[finding] → [what to do about it]

## Pass 2 — machinery
[finding] → [what to do about it]

## Pass 3 — evolution
[finding] → [what to do about it]

## Growth — worth building, worth cutting
[recommendation] — [evidence, counted] — [suggested first step]

## The fix list
Every finding above as one checkbox line, weight-labeled, in checklist
order. Ticks get dated as fixes land. Recommendations never appear here.
```

Score honestly, against the anchors above, the same way every month. And
write the whole report in plain business English — file paths are fine,
jargon is not. If a sentence wouldn't land with a busy owner, rewrite it.

## Headless mode — when nobody is in the chair

If this audit runs on a schedule rather than in conversation, it measures
and reports only. It fixes nothing, asks nothing, and builds nothing.
Write the report into `audits/`, and leave the fix list untouched for the
owner to walk through when they next open the folder. Also verify your own
heartbeat while you are here: if the last scheduled run is missing from
`audits/`, say so at the top of the report.
