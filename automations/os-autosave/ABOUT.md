# The hourly backup — this OS saves itself

## What it does

Every hour, this folder commits whatever changed and pushes it to the
owner's private GitHub repo. That is all it does.

It exists because the most valuable thing here is what the system learned
this week, and the most common way to lose that is a laptop that doesn't
come back on. The handoff skill is the save the owner runs on purpose; this
is the net underneath it, for the afternoon nobody closed properly.

## When it runs

Every hour, while the owner is logged in to their computer. A missed hour
just waits for the next one.

## Where it lives

Not in this folder. It is a scheduled job on the owner's own machine, made
of one command, and it runs git directly with no script file and no AI
involved. `SETUP.md` beside this file has the exact command for Windows and
Mac, plus how to check it and how to remove it.

Because no model runs, it costs nothing. It does not read the folder, does
not think about it, and cannot change a file.

## Trust status

Automated from day one. That is unusual here, and it is deliberate: this job
cannot do anything except save. It never writes a file, never runs a skill,
never sends anything, never touches a connected tool.

## What "working" looks like

The repo on GitHub shows commits called `autosave` with recent timestamps.
If the newest commit in the repo is more than a day old and the owner has
been working, the job has died quietly. The monthly audit checks exactly
this.

## Three commit types, so the history reads clearly

- `autosave` — this job. Nobody looked at it.
- Plain English — the handoff skill, or the owner. Something happened and it
  says what.
- `self-edit:` — the system changing how it works, with the evidence and how
  to undo it (contract law 11).

## Logs

None. A one-line commit history is the log, and it lives on GitHub. If this
job ever grows a script, the script and its logs go in the sibling code
folder beside this OS (contract law 10), and this file says where.
