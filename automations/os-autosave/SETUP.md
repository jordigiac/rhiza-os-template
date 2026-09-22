# The hourly backup — setup

One command. No script file, no downloads. Run it once.

**Before you run it:** this folder must already be connected to your own
private GitHub repo, and one push must have worked. Onboarding Part 0 does
that with you and checks it. If pushing doesn't work yet, this will fail
every hour, and you will not notice.

---

## Windows

Open PowerShell. Change the folder path on the first line to your own, then
paste the whole block:

```powershell
$folder = "C:\Users\YOU\Documents\your-os-folder"
$tr = "cmd /c cd /d \`"$folder\`" && git add -A && (git diff --cached --quiet || git commit -m autosave) && git push"
schtasks /create /tn "OS hourly backup" /tr $tr /sc hourly /f
schtasks /run /tn "OS hourly backup"
```

That last line runs it immediately, so you find out now instead of in an
hour. Wait ten seconds, then go to **How to check it worked** below.

To run it by hand any time: `schtasks /run /tn "OS hourly backup"`
To see it: `schtasks /query /tn "OS hourly backup" /fo LIST /v`
To remove it: `schtasks /delete /tn "OS hourly backup" /f`

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
(crontab -l 2>/dev/null; echo "0 * * * * cd \"$FOLDER\" && /usr/bin/git add -A && (/usr/bin/git diff --cached --quiet || /usr/bin/git commit -m autosave) && /usr/bin/git push") | crontab -
```

Then run it once by hand, right now, so you find out immediately instead of
in an hour:

```bash
cd "$FOLDER" && git add -A && (git diff --cached --quiet || git commit -m autosave) && git push ; echo "result: $?"
```

`result: 0` means it worked. Anything else means it did not.

To see the schedule: `crontab -l`
To remove it: `crontab -l | grep -v autosave | crontab -`

If the by-hand run works but the hourly one never does, macOS is blocking
scheduled jobs from reaching your Documents folder. System Settings →
Privacy & Security → Full Disk Access, and add Terminal. That is a one-time
thing.

---

## How to check it worked

**Do this now, not in an hour.** A backup whose only test takes an hour is a
backup nobody ever tests.

1. Change something small in the folder and save it.
2. Run it by hand with the command above.
3. Wait ten seconds, then open your repo on GitHub. There should be a new
   commit called `autosave` carrying your change.

On Windows you can also read the result the job itself recorded:

```powershell
schtasks /query /tn "OS hourly backup" /fo LIST /v | Select-String "Last Result"
```

**`Last Result: 0` means it worked. Any other number means it failed.**

**If the commit is not on GitHub, the backup is not working, whatever else
looks healthy.** Do not move on. The usual causes, in order: the folder path
has a typo, the repo has no remote yet, or GitHub is asking for a login your
computer hasn't saved. Ask your OS to walk through those three with you, in
that order.

---

## Two deliberate choices, so nobody "fixes" them

**The commit message is just the word `autosave`.** Putting a date in it
means putting a `%` in the command, and `%` is a special character in both
Windows scheduled tasks and Mac cron. It breaks things quietly: the job
appears to run and nothing is ever saved. Git already records the exact time
of every commit.

**Every step is chained with `&&`, and the job never pulls.** Both matter:

- `&&` means a failure stops the chain and the job reports a failure. The
  earlier version used separators that ran the next command regardless,
  so a wrong folder path produced a perfectly healthy-looking task that had
  never saved anything. Tested and confirmed before this was changed.
- **No pull.** Pulling unattended can hit a conflict, and a conflict would
  leave your folder stuck mid-merge with every later hour failing too. This
  job only saves. When you close a session properly, the handoff does the
  pull carefully and stops to ask you if anything disagrees.

## If it breaks

Nothing is lost. Everything is still on your computer, and the next proper
close will push all of it. A dead backup is a quiet problem, not an urgent
one, which is exactly why the monthly audit goes looking for it.

## What it never does

It never writes a file, never runs a skill, never sends anything, never
touches a connected tool, and never deletes. It saves, and that is the whole
job.
