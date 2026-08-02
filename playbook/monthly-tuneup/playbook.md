# Monthly tune-up — Jordi's checklist

*v1 draft. This is the SOP the retainer's second half runs on. It matures
alongside the audit skill — once the skill exists, steps marked (audit) are
its output, read rather than hand-checked. Target: a few hours per client.*

## Prep

- [ ] Pull the client repo latest. Skim STATE.md and decisions.md since last
      tune-up — know what happened before judging the system.

## The health pass

- [ ] (audit) Routing check: every path CLAUDE.md's table points to exists;
      nothing on disk is unreachable from the front desk.
- [ ] (audit) New-hire test: cold-open the folder — can you orient and route
      in three reads or fewer?
- [ ] (audit) Truth check: stale files (30+ days untouched that shouldn't
      be), contradictions between files, duplicated facts. One home per fact.
- [ ] (audit) Bloat check: crowded knowledge files, oversized contracts.
      Split or trim; keep the $20/month token story true.
- [ ] (audit) Four C's score, out of 100, saved with date — the trend line
      is the retainer's proof of care.

## The machinery pass

- [ ] Every automation: logs reviewed, ran clean, ABOUT.md still accurate.
- [ ] Ladder moves: promote what's consistently passing its checks
      (beta → proving → automated); demote or pause anything misbehaving.
- [ ] Every skill: still invoked, still works. Fix or retire.
- [ ] Connections: keys valid, permissions still minimal.

## The evolution pass

- [ ] Does the structure still fit the business? Resize knowledge/ (split
      into folders with a small index when crowded). Propose new workspaces
      only for work that's genuinely repeating.
- [ ] Refresh STATE.md's Up next — what's being built, expected when.

## Close

- [ ] Write the tune-up report in plain English (what was checked, fixed,
      changed, the score). Deliver it.
- [ ] Any questions for the owner: one short list, answerable by text.
- [ ] Commit and push. Log notable changes in the client's decisions.md.
- [ ] Add anything learned to this checklist.
