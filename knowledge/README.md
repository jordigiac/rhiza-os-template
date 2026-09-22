# knowledge/ — what this OS knows about the business

Two layers, and the difference between them matters.

## The core — `knowledge/core/`

What the business *is*. What it does, who it serves, what it sells at what
price, how the owner sounds, who does what on which tools.

**Every draft this system makes gets built from these files.** Before it
writes an email, plans a launch, or fills a tracker, it reads core. That is
why core is allowed to be boring and exact: a price quoted from here is
right, and a price remembered from a chat three weeks ago is a coin flip.

**Core changes only when the owner says so** (contract law 9). When the
system hears something new that contradicts core, it says so out loud in one
line and waits. It never edits these files quietly.

| File | What it holds |
|---|---|
| `business-profile.md` | What the business does, why it exists, how money comes in |
| `audience.md` | Who it serves, what they want, how they say it |
| `offers.md` | Every offer: price, link, format, dates, status |
| `voice.md` | How the owner sounds, described |
| `voice-samples.md` | How the owner sounds, proven — real things they wrote |
| `team-and-tools.md` | Who does what; which tool does which job |

*If this business ever grows to a second person with their own OS, core is
what the two copies share. That is why it has its own folder.*

## The working knowledge — everything else in here

What the system learns as the business talks. Stated facts get filed the
moment they're said, dated, out loud (contract law 1).

| File or folder | What it holds |
|---|---|
| `owner-profile.md` | Who the owner is, how they work, their hard lines |
| `priorities.md` | The next 90 days |
| `problem-list.md` | Repeated work that hurts — the shortlist for what gets built |
| `clients/` | One file per client, or a roster |
| `partners/` | JV partners: history, list size, what they need from you |
| `programs/` | What you teach, module by module |

## Rules for this whole folder

**One home per fact.** If something is written here, other files point at it
instead of repeating it. Two copies of a price is how a wrong one ships.

**Every fact file opens with a "Last confirmed:" line** — the date a human
last said its contents are still true. Live capture and the handoff sweep
refresh it when facts change, the checkup refreshes the oldest, and the audit
counts the ages. No date means never confirmed, which puts it first in line
at the next checkup.

**Paths are load-bearing.** Skills and checks point at these files by name.
Before moving or renaming one, search the whole folder for anything that
points at it and fix those too, in the same breath.

**Add, don't rewrite.** When new information arrives, add it and mark what it
replaces. Rewriting a file wholesale loses detail nobody notices is gone.
Consolidation is a deliberate job the owner asks for, not a tidy-up.

## Where new things go

| When this arrives | It goes here |
|---|---|
| A new offer, course, or event | `core/offers.md` (a new block) |
| A price change | `core/offers.md`, on the owner's word |
| Something a customer said, word for word | `core/audience.md` |
| Something the owner wrote that sounds like them | `core/voice-samples.md` |
| A new team member, contractor, or tool | `core/team-and-tools.md` |
| A new client | `clients/` |
| A new JV partner, or a promo that ran | `partners/` |
| Curriculum, session plans, materials | `programs/` |
| "Ugh, I have to do this again every week" | `problem-list.md` |
| A decision and its why | `../decisions.md` |
| Something unresolved | `../OPEN-QUESTIONS.md` |
