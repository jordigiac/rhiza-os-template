# The hourly backup — setup

One command. No script file, no downloads. Run it once.

**Before you run it:** your OS folder must already be a git repo connected to
your own private GitHub, and one push must have worked. Onboarding Part 0
does this with you and checks it.

---

## Windows

Open PowerShell and paste this, with your own folder path:

```powershell
$folder = "C:\Users\YOU\Documents\your-os-folder"
$cmd = "cd /d `"$folder`" && git add -A && git commit -m ""autosave: %DATE% %TIME%"" && git push || (git pull --rebase && git push)"
schtasks /create /tn "OS hourly backup" /tr "cmd /c $cmd" /sc hourly /f
```

To check it exists: `schtasks /query /tn "OS hourly backup"`
To remove it: `schtasks /delete /tn "OS hourly backup" /f`

---

## Mac

Open Terminal and paste this, with your own folder path:

```bash
FOLDER="/Users/you/Documents/your-os-folder"
(crontab -l 2>/dev/null; echo "0 * * * * cd \"$FOLDER\" && git add -A && git commit -m \"autosave: \$(date '+%Y-%m-%d %H:%M')\" && git push || (git pull --rebase && git push)") | crontab -
```

To check it exists: `crontab -l`
To remove it: `crontab -e`, delete that line, save.

---

## How to verify it works

1. Change something small in the folder and save it.
2. Wait for the top of the next hour.
3. Open your repo on GitHub. There should be a new commit starting with
   `autosave:`.

If there isn't, the most common causes are: the folder path has a typo, the
repo has no remote yet, or GitHub is asking for a login your computer hasn't
saved. Ask your OS to help you check, in that order.

## If it breaks

Nothing is lost. Everything is still on the computer, and the next handoff
will push it all. A dead backup is a quiet problem, not an urgent one, which
is exactly why the monthly audit looks for it.

## What it never does

It never writes a file, never runs a skill, never sends anything, never
touches a connected tool, and never deletes. It saves, and that is the whole
job.
