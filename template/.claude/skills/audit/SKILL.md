---
name: audit
description: Read-only health check of THIS operating system folder. Checks routing, files, automations, and skills against reality, scores the Four C's, and writes a dated report into audits/. Use for /audit or "how is the system doing". Never audits the computer itself. Never fixes anything.
---

# Audit — is this OS still telling the truth?

Read-only, by oath: never fix, rename, move, or delete anything. Files and
wikis are claims about what exists; this skill checks every claim against
reality and reports. Fixing happens deliberately on the monthly maintenance
pass, never silently by this skill.

The report is built to be worked top to bottom: every finding pairs with
what to do about it, so the maintenance pass can go down the line.

## Steps

1. Read the previous report in audits/ (if any) so the new one can show
   what changed.
2. Run the three passes below, collecting findings.
3. Write the report to `audits/YYYY-MM-DD-audit.md` in the format at the
   bottom. Never edit a past report.

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
- Bloat check: CLAUDE.md over 60 lines, any knowledge file that has grown
  crowded, any workspace contract over 80 lines.

## Pass 2 — machinery (does everything still run?)

- Each automation (skip `_template` folders; those are blank starters):
  ABOUT.md matches reality (schedule, location, ladder status), logs show
  clean runs since the last report, SETUP.md's verification step still
  passes as described.
- Each skill: present, listed in the skills README, and actually referenced
  or used. Flag anything unused or broken.
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

## Opportunities — evidence only, operator-only, decisions are humans' work

This section is for whoever maintains the system. It never surfaces in
conversation with the owner — the no-proposing rule holds; this report is
where the evidence waits for the humans' next planning conversation.

Scan STATE.md history, decisions.md, and handoff commits for patterns:
the same manual task appearing session after session, an automation whose
logs show growing load, a workflow the owner keeps mentioning. List each
with its evidence. Suggest nothing beyond the evidence; deciding what to
build belongs to people, not to this report.

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
  actually used. The five preloads are the floor: 0, in every install, always.
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

## Opportunities
[pattern] — [evidence]

## The fix list
Every finding above as one checkbox line, in checklist order.
```

Score honestly, against the anchors above, the same way every month. And
write the whole report in plain business English — file paths are fine,
jargon is not. If a sentence wouldn't land with a busy owner, rewrite it.
