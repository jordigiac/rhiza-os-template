---
name: audit
description: The truth check. Read-only monthly health report - verifies every claim in the OS against reality, scores the Four C's, surfaces automation opportunities from evidence, and writes a dated report into audits/. Use when Jordi runs /audit or asks how the system is doing. Never fixes anything.
---

# Audit — is this OS still telling the truth?

Read-only, by oath: never fix, rename, move, or delete anything. Files and
wikis are claims about what exists; this skill checks every claim against
reality and reports. Fixing is Jordi's job at the tune-up.

The report mirrors Jordi's tune-up checklist section for section, so he can
put the two side by side and go down the line.

## Steps

1. Read the previous report in audits/ (if any) so the new one can show
   what changed.
2. Run the three passes below, collecting findings.
3. Write the report to `audits/YYYY-MM-DD-audit.md` in the format at the
   bottom. Never edit a past report.

## Pass 1 — health (does the structure tell the truth?)

- Routing check: every path in CLAUDE.md's map and routing table exists on
  disk, and everything on disk is reachable from the front desk. Check both
  directions. Confirm AGENTS.md is identical to CLAUDE.md.
- New-hire test: open the folder cold. Can a stranger orient and route to
  any task in three reads or fewer? Name where they would get lost.
- Truth check: files untouched 30+ days that claim to be current,
  contradictions between files, the same fact written in two places,
  leftover [BRACKETED] placeholders.
- Bloat check: CLAUDE.md over 60 lines, any knowledge file that has grown
  crowded, any workspace contract over 80 lines.

## Pass 2 — machinery (does everything still run?)

- Each automation: ABOUT.md matches reality (schedule, location, ladder
  status), logs show clean runs since the last report, SETUP.md's
  verification step still passes as described.
- Each skill: present, listed in the skills README, and actually referenced
  or used. Flag anything unused or broken.
- Connections: each reference file names a real .env key in .env.example
  terms, and describes limits that still match how it is used.

## Pass 3 — evolution (does the system still fit the business?)

- Knowledge sized right: files that should split into a folder with an
  index, or folders that shrank back to a file.
- Workspaces still earn their place: is the work still repeating?
- STATE.md's Up next is current, with dates the owner can trust.

## Opportunities — evidence only, decisions are humans' work

Scan STATE.md history, decisions.md, and handoff commits for patterns:
the same manual task appearing session after session, an automation whose
logs show growing load, a workflow the owner keeps mentioning. List each
with its evidence. Suggest nothing beyond the evidence; Jordi and the owner
decide on the monthly call.

## Report format

```
# Audit — YYYY-MM-DD

Four C's: NN/100 (Context NN/25, Connections NN/25, Capabilities NN/25,
Cadence NN/25). Last month: NN. One-line verdict.

## Pass 1 — health
[finding] → [what Jordi should do]

## Pass 2 — machinery
[finding] → [what Jordi should do]

## Pass 3 — evolution
[finding] → [what Jordi should do]

## Opportunities
[pattern] — [evidence]

## The fix list
Every finding above as one checkbox line, in checklist order.
```

Score honestly. A fresh install scoring 50 is normal; the trend is the point.
