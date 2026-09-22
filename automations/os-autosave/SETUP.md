# The hourly backup — setup

One command. No script file, no downloads. Run it once.

**Before you run it:** this folder must already be connected to your own
private GitHub repo, and one push must have worked. Onboarding Part 0 does
that with you and checks it. If pushing doesn't work yet, this will fail
every hour, quietly, forever.

---

## Windows

Open PowerShell. Change the folder path on the first line to your own, then
paste the whole block:

```powershell
$folder = "C:\Users\YOU\Documents\your-os-folder"
$tr = "cmd /c cd /d `"$folder`" && git add -A && git commit -m autosave & git pull --rebase & git push"
schtasks /create /tn "OS hourly backup" /tr $tr /sc hourly /f
```

Check it exists: `schtasks /query /tn "OS hourly backup"`
Run it once, right now, to prove it works: `schtasks /run /tn "OS hourly backup"`
Remove it: `schtasks /delete /tn "OS hourly backup" /f`

---

## Mac

Open Terminal. Change the folder path on the first line to your own, then
paste both lines:

```bash
FOLDER="/Users/you/Documents/your-os-folder"
(crontab -l 2>/dev/null; echo "0 * * * * cd \"$FOLDER\" && /usr/bin/git add -A && /usr/bin/git commit -m autosave; /usr/bin/git pull --rebase; /usr/bin/git push") | crontab -
```

Check it exists: `crontab -l`
Remove it: `crontab -e`, delete that line, save.

If it never seems to run, macOS is probably blocking scheduled jobs from
reaching your Documents folder. System Settings → Privacy & Security → Full
Disk Access, and add Terminal. That is a one-time thing.

---

## Why the commit message is just the word "autosave"

It is deliberate, and worth not "improving." Putting a date in the message
means putting a `%` in the command, and `%` is a special character in both
Windows scheduled tasks and Mac cron. It breaks the command in ways that
don't announce themselves: the job appears to run, and nothing ever saves.

Git already records the exact time of every commit. The message doesn't need
to repeat it.

## How to verify it works

1. Change something small in the folder and save it.
2. Run the job by hand using the command above, or wait for the top of the
   hour.
3. Open your repo on GitHub. There should be a new commit called `autosave`.

If there isn't, the usual causes, in order: the folder path has a typo, the
repo has no remote yet, or GitHub is asking for a login your computer hasn't
saved. Ask your OS to help you check, in that order.

## If it breaks

Nothing is lost. Everything is still on the computer, and the next handoff
will push all of it. A dead backup is a quiet problem, not an urgent one,
which is exactly why the monthly audit goes looking for it.

## What it never does

It never writes a file, never runs a skill, never sends anything, never
touches a connected tool, and never deletes. It saves, and that is the whole
job.
