# skills/ — the OS's preset toolbox

Five preloaded skills ship with every install. Together they serve the one
job: keep the system's knowledge of the business complete and true, and
lose nothing.

Every skill lives complete in this folder as markdown — nothing to install
on the machine, nothing outside the OS. The toolbox travels with the folder
and works in any Claude surface: the front desk carries the fallback (name
a skill; if nothing fires automatically, its SKILL.md gets read and
followed), so the OS survives interface changes. Only automation code lives
outside, in its own lean repo — `automations/` holds the map.

- **onboard** — installs the owner into their OS: the self-paced setup
  conversation, resumable across sessions, done at the finish line where
  setup/ deletes itself. Once setup/ is gone it never runs again.
- **handoff** — the save button, and the owner's one command. Closes a
  session with nothing lost: state updated, decisions logged, stated facts
  filed, committed.
- **checkup** — the five-minute conversation that keeps knowledge true:
  the oldest and most load-bearing beliefs, confirmed, corrected, or
  rejected by the owner.
- **audit** — the truth check on the system itself. Read-only monthly
  report: does everything still match reality, scored against fixed
  anchors. Its report drives the monthly maintenance pass.
- **humanizer** — the voice guard. Any draft meant for a person runs
  through it, so nothing leaves this OS sounding like AI. (Vendored from
  blader/humanizer, MIT, with Rhiza's structural additions.)

There is no "level-up" skill — surfacing what to automate next is a human
conversation, not software.

Skills the owner uses day to day are custom work, added here as the
business needs them.
