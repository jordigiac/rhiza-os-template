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
$tr = "cmd /c cd /d \`"$folder\`" && git add -A && git commit -m autosave & git pull --rebase & git push"
schtasks /create /tn "OS hourly backup" /tr $tr /sc hourly /f
schtasks /run /tn "OS hourly backup"
```

That last line runs it immediately, so you find out now instead of in an
hour. Give it ten seconds, then check the next section.

Check it exists later: `schtasks /query /tn "OS hourly backup"`
Remove it: `schtasks /delete /tn "OS hourly backup" /f`

> **Those backslashes before the quotes are not a typo.** Windows strips
> ordinary quotes out of a scheduled command, which splits your folder path
> at the first space and saves nothing. Tested: without them, a path like
> `My Business OS` fails with `ERROR: Invalid argument/option - 'Business'`.

---

## Mac

Open Terminal. Change the folder path on the first line to your own, then
paste both lines:

```bash
FOLDER="/Users/you/Documents/your-os-folder"
(crontab -l 2>/dev/null; echo "0 * * * * cd \"$FOLDER\" && /usr/bin/git add -A && /usr/bin/git commit -m autosave; /usr/bin/git pull --rebase; /usr/bin/git push") | crontab -
```

Then run the backup once by hand, right now, so you find out immediately
instead of in an hour:

```bash
cd "$FOLDER" && git add -A && git commit -m autosave; git pull --rebase; git push
```

Check the schedule exists: `crontab -l`
Remove it: `crontab -l | grep -v autosave | crontab -`

If the manual run works but the hourly one never does, macOS is blocking
scheduled jobs from reaching your Documents folder. System Settings →
Privacy & Security → Full Disk Access, and add Terminal. That is a one-time
thing.

---

## Why the commit message is just the word "autosave"

It is deliberate, and worth not "improving." Putting a date in the message
means putting a `%` in the command, and `%` is a special character in both
Windows scheduled tasks and Mac cron. It breaks the command in ways that
don't announce themselves: the job appears to run, and nothing ever saves.

Git already records the exact time of every commit. The message doesn't need
to repeat it.

## How to verify it works — right now, not in an hour

A backup whose only test takes an hour is a backup nobody ever tests.

1. Change something small in the folder and save it.
2. Run it immediately, using the run command above.
3. Wait ten seconds, then open your repo on GitHub. There should be a new
   commit called `autosave` carrying your change.

**If that commit is not there, the backup is not working, whatever the
schedule says.** Do not move on. The usual causes, in order: the folder path
has a typo or a space that broke the command, the repo has no remote yet, or
GitHub is asking for a login your computer hasn't saved. Ask your OS to walk
through those three with you, in that order.

*(The job runs a pull and a push every hour even when nothing changed. That
is deliberate: it costs a second, and it picks up anything you saved on
another computer.)*

## If it breaks

Nothing is lost. Everything is still on the computer, and the next handoff
will push all of it. A dead backup is a quiet problem, not an urgent one,
which is exactly why the monthly audit goes looking for it.

## What it never does

It never writes a file, never runs a skill, never sends anything, never
touches a connected tool, and never deletes. It saves, and that is the whole
job.
