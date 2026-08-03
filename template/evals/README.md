# evals/ — how quality works in this OS

Three layers, from always-on to monthly:

1. **Standing checks** (`standard/`) run on the OS's everyday output — any
   draft, any claim, every session close. No setup, no maintenance; they
   ship with the system.
2. **Custom exams** — every automation and custom skill gets its own folder
   here (copied from `_template/`): a dataset of test cases, scorers that
   define what done looks like, and dated scorecards. Jordi builds these at
   build time; they are the graduation exams of the trust ladder. Nothing
   moves from beta to automated without passing its exam consistently.
3. **The audit** is the eval of the system itself — monthly, read-only,
   reports in `audits/`.

Verdicts are always **pass or fail plus a short critique** — never score
scales. A critique holds the nuance; the verdict holds the line.

Jordi maintains this folder. The owner benefits without touching it — and
owns it: the datasets and scorecards are this business's records, and they
stay in this OS.
