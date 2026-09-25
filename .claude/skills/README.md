# skills/ — the OS's preset toolbox

The skills that ship with every install. Together they serve one job: keep
this system's knowledge of the business complete and true, lose nothing, and
sound like the owner when it writes.

Every skill lives complete in this folder as markdown. Nothing to install on
the machine, nothing outside the OS. The toolbox travels with the folder and
works in any Claude surface: the front desk carries the fallback, so if the
owner names a skill and nothing fires automatically, its SKILL.md gets read
and followed. The OS survives interface changes.

Only automation code lives outside, in the sibling folder beside this one.
`automations/` holds the map.

## What ships

- **onboard** — installs the owner into their OS: the self-paced setup
  conversation, resumable across sessions, done at the finish line where
  `setup/` deletes itself. Once `setup/` is gone it never runs again.
- **pickup** — the session opener. Where we were, what's next, what's waiting
  on you. Read-only; it changes nothing.
- **handoff** — the session closer, and the owner's one command. Files what
  they said, logs decisions, updates the board, takes the journal note, then
  commits and pushes safely.
- **write-like-me** — drafts anything in the owner's voice, from real samples
  of their writing. Everything it makes is a draft.
- **humanizer** — the voice guard. Anything meant for a person runs through
  it, so nothing leaves sounding like AI. (Vendored from blader/humanizer,
  MIT, with additions.)
- **checkup** — the five-minute conversation that keeps knowledge true: the
  oldest and most load-bearing beliefs, confirmed, corrected, or rejected by
  the owner.
- **audit** — the truth check on the system itself. A read-only monthly
  report, scored against fixed anchors, that then fixes only what the owner
  approves.

There is no "level-up" skill. Surfacing what to automate next is a
conversation, not software.

Skills the owner uses day to day are custom work, added here as the business
needs them.

## Routing is the system's job

The owner describes what they want in plain words. The system picks the
skill. Nobody should have to memorise a name to get their launch emails
written, and a skill that only fires when its name is typed is a skill that
doesn't exist for most people.

## How to write or edit one

- **Critical rules go at the top of the file.** When a long conversation gets
  compacted, the bottom of a file is what gets cut first. A guardrail buried
  under the steps goes missing exactly when the session is long enough to
  need it.
- **Edit by delta, not by rewrite.** Change the lines that are wrong. A
  wholesale rewrite silently drops hard-won detail nobody remembers putting
  there.
- **Prune while you're in there.** If a step has never once applied, cut it.
- **Keep it under about 5,000 words.** Past that, a skill stops being read in
  full and starts being skimmed, which is the same as being wrong.
- **Anything that writes for a person ends the same way:** the Gate in
  `evals/`, then the humanizer, then a draft for the owner's yes.
