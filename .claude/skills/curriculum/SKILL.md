---
name: curriculum
description: Designs a course, program, or training from a topic and an audience. Works backward from what students will be able to do, then builds modules, lessons, action steps and checkpoints around the owner's own method, fitted to the real time available. Drafts the outline first for the owner's okay, then the lesson detail. Use when the owner wants to create, outline, restructure, or expand a course, group program, workshop, challenge content, training, or "what should I teach in week 3". Saves into the program's own file in knowledge/programs/. launch-facts owns the offer's price and dates.
metadata:
  version: 2.0.0
  fitted-from: curriculum 1.2.0 (Jonathan's draft), fitted to the template 2026-09-29
---

# Curriculum — the map of what the course teaches

The owner knows how to get people results. This skill organizes that know-how
into a course: a clear promise, modules that build toward it, and lessons
with action steps. It works backward: first what students will be able to
do, then how you'll know they can, then what to teach.

**Who owns what:** curriculum owns what the course teaches (promise,
modules, lessons, outcomes). launch-facts owns the offer's price, dates and
links. messaging owns sales copy, and may quote the course's promise and
modules from here. Curriculum never sets a price, date or link.

**Where it lives:** one file per program, `knowledge/programs/<program>.md`,
which is where the template keeps what a coach teaches. The offer's price
and sales link stay in `knowledge/core/offers.md`; the teaching lives here.
If the program file already exists (room link, run dates, what students
ask), curriculum owns only its *Curriculum* part and leaves the rest as it
is.

## Critical rules

1. **The owner's method is the content.** Look for what the owner already
   has, in this conversation, knowledge/ and anything they share:
   frameworks, steps, principles, their terms for things, teaching habits,
   stories, examples, exercises, and the order they teach in. Build on
   that. Label where material came from:
   - **Owner's** (no label): it comes from the owner.
   - `(suggested)`: AI-made structure, exercise, example or sequence.
   - `(adapted, owner okayed YYYY-MM-DD)`: the owner's material that you
     reorganized, and they approved the change.
   A gap stays a gap. Mark it `(suggested)` or `TBD`, say what's missing,
   and ask for their version. Never pass off a generic best practice, or
   an invented story or client example, as the owner's method.
2. **Outcomes and checkpoints you can check.** Module outcomes and lesson
   goals use verbs a student can be seen doing: list, write, choose,
   draft, practice, decide, map, pitch. Not "understand", "learn", "know",
   "appreciate" or "explore". A checkpoint is evidence the owner can
   inspect: a finished artifact, a draft, a decision made, a skill shown, a
   step done. "Feels confident" or "understands" isn't a checkpoint; turn
   it into what they'd produce.
3. **Promise what students will do, not results nobody controls.** The
   promise can name a real transformation ("build a repeatable way to find
   clients") as long as it breaks into observable capabilities, one per
   module ("define the client, write the offer, plan the outreach, run the
   first campaign"). "You'll leave with a written pivot plan and your
   first 3 conversations booked" is fine. "You'll land a new job in 8 weeks", "double your income" or any
   health, legal or financial result is not. If the owner asks for one,
   explain in one line and offer the do-based version. A real result the
   owner has had with clients can be mentioned as their story, not as a
   promise.
4. **Fit the real time and the real workload.** Count the clock: sessions
   × length, plus homework. Then check the load, since a plan can fit the
   clock and still be too much: new big ideas per session (1–3 is plenty),
   how hard the assignments are, whether two big assignments land in the
   same week. If it's too much, simplify, split, move or merge, and say
   what moved. Never cram to keep every topic.
5. **Outline first, detail second.** Draft the promise, modules and module
   outcomes. Stop for the owner's okay. Only then write lesson detail, a
   few modules at a time. Never write the whole course in one pass.
6. **Approving a structure isn't claiming an idea.** When the owner okays
   the outline, they're approving the structure. Anything marked
   `(suggested)` stays suggested unless the owner adopts it as theirs
   ("yes, that's how I teach it", "make that part of my method"). Then it
   becomes `(adapted, owner okayed …)` or loses its label.
7. **Stable IDs.** Modules are M1, M2…; lessons M1.L1, M1.L2…. Once
   given, an ID never changes, because talks, session notes and the
   owner's own notes point to it. A dropped module or lesson stays, marked `Cancelled`.

## Inputs

- The owner's request: topic, audience, format, length, delivery.
- `knowledge/core/audience.md`: who the business serves, in their words.
- `knowledge/core/offers.md`: the offer this course belongs to (format,
  length, delivery).
- `knowledge/core/voice-samples.md`, `knowledge/core/voice.md` and
  `knowledge/owner-profile.md`: how they teach and talk.
- Any frameworks, notes, past slides or transcripts the owner shares.
- `knowledge/programs/<program>.md`, if it exists.
- `references/course-design.md` (this skill's folder): backward design, outcome verbs, lesson shape, pacing.

## Steps

1. **Pin down the basics.** From the request and knowledge/: who it's for
   (and who it isn't for), the format (group program, self-paced course,
   one-day workshop, challenge), how many sessions and how long each, live
   or recorded, and the owner's method. Anything missing that changes the
   design is `TBD` and goes in the questions. Don't stop for it. Draft
   with what's known.
2. **Write the promise.** One sentence: by the end, students will be able
   to [do something checkable]. Then 3–5 "who it's for" and 2–3 "who it's
   not for" lines, from `core/audience.md` or the owner.
3. **Work backward to modules.** What must a student be able to do along
   the way to get there? Each is a module with one outcome and one
   checkpoint (evidence the owner can see: "has a written list of 3 target
   roles"). **Order by dependency:** what they must know or have made
   first, and which later exercise needs which earlier output. No
   activity before its prerequisites. If the owner's method breaks the
   usual order on purpose, keep their order and note why if known. Map
   modules to the owner's framework if there is one; if not, mark the
   structure `(suggested)`.
4. **Check it holds together** (for the outline, and again for each lesson
   batch):
   - Promise → module outcomes → lessons → practice and action step →
     checkpoint. Each link is real; nothing floats.
   - Modules come in dependency order.
   - Clock and workload pass (rule 4). Count the weeks: every module sits in
     a real session, no two modules share one unless planned, and the
     count matches the sessions the owner gave.
   - Every outcome and checkpoint is observable (rule 2); the promise is
     within the student's control (rule 3).
   - Provenance labels are right: nothing suggested is shown as the owner's.
   - No price, date, link or sales copy (other skills own those).
5. **Save the outline** into `knowledge/programs/<program>.md` (plain name,
   e.g. `re-entry-lab.md`), under a *Curriculum* heading, status Draft,
   using the template. Create the file if it doesn't exist; if it does,
   add or update only the *Curriculum* part. Add the file to the programs
   folder's README if it isn't listed.
6. **Reply.** Plain words: "the outline", "your offers file". Say where
   the outline lives once, in plain words ("it's in your programs folder,
   under Re-Entry Lab"). Give the promise, the module list (one line each:
   outcome + checkpoint), what's suggested vs. the owner's own method, the
   time fit, and **at most 5 questions** (their framework, stories,
   must-teach topics first). Everything else you'd ask goes under *Still
   needed* on the page, not in the reply. Where you'd recommend something,
   apply it as `(suggested)` rather than asking. Ask for an okay on the outline before lesson detail.
   The reply runs the Gate (`evals/gate.md`) like anything a person reads.
7. **On the owner's okay,** mark the outline Approved (dated) on the page
   itself, and set the file's *Last confirmed* line to today. Then write
   lesson detail 2–3 modules at a time, in the lesson shape from the
   reference: goal, teaching (the key points, from the owner's material;
   gaps as `[Your story or example needed]`), practice, action step,
   evidence (only if it differs from the module checkpoint), and minutes. Keep them distinct: **teaching** is what the owner explains
   or shows, **practice** is what students do in the session, the **action
   step** is what they do afterward, and **evidence** is what proves it got
   done. Skip a part when a lesson truly doesn't need it. Don't invent an
   activity to fill the slot. Every lesson follows the standing habits on
   the *Method* line (a hot seat at the end of every call means every call's
   lessons leave time for it). A lesson's minutes are its own teaching and
   practice time, never the whole session. Each module that's a live
   session gets a **Session time** line that adds up to the session length,
   with the standing habits in it: `Session time: 90 min = open 5 + M3.L1 55
   + hot seat 25 + close 5 (suggested)`. Add it up before saving. Stop after
   each set for review.

## When the owner changes something

- Changing an **Approved** outline (a module added, dropped, reordered, or
  a new promise): update it, keep IDs (never renumber; a removed item
  stays, marked `Cancelled`), log it, set status back to Draft for the
  owner's okay. Then list what may now be stale (lessons, exercises,
  checkpoints, and any talk plans or drafts built from those IDs) without
  editing anything another skill owns. Say what needs a review and by which
  skill.
- **Edits to lesson detail** apply to that lesson only.
- **Course decision or standing practice?** "For this course, end every
  session with a hot seat" or "week 8 is a celebration" is a decision for
  this course. It goes on the *Method* line only. "I always end my calls
  with a hot seat" is a standing practice. It's filed in
  `knowledge/owner-profile.md` too, dated, in the owner's words, and said
  out loud (contract law 1). Stated facts about
  the audience ("my people won't do more than an hour of homework") are
  filed as facts. If you can't tell which it is, ask; don't file it.

## Curriculum template (inside `knowledge/programs/<program>.md`)

```markdown
# [Program name]

*Last confirmed: [set when the owner approves the outline]*

*(The price and sales link live in `knowledge/core/offers.md`. The
teaching lives here.)*

## Curriculum

*Status: Draft / Approved YYYY-MM-DD · Format: [8 weekly live calls, 90 min] · Updated YYYY-MM-DD*

### Promise
By the end, students will be able to …

**For:** …  **Not for:** …

### Modules
| ID | Module | Outcome (students can…) | Checkpoint | Sessions / time |
|---|---|---|---|---|
| M1 | … | … | … | Week 1, 90 min |

**Time check:** [total needed vs. available]
**Method:** [the owner's framework, or "structure suggested, owner's method needed"]

### Lessons
#### M1 — [Module name]
Session time: [90] min = open [n] + M1.L1 [n] + [standing habit] [n] + close [n] (suggested)
##### M1.L1 — [Lesson name] · [minutes of this lesson only]
- Goal: students can …
- Teaching: … (owner's) / … (suggested)
- Practice: …
- Action step: …
- Evidence: … (if different from the module checkpoint)

### Still needed
- …

### Change log
| Date | What changed | Why | IDs affected | Needs review |
|---|---|---|---|---|
```

## Needs the owner's yes

- Approving the outline, before lesson detail.
- Any suggested structure, story or example becoming "theirs".
- Changing an Approved outline.

## Guardrails

- Plain English in the reply. Say where the outline lives once, in plain
  words.
- No prices, dates, links or sales copy. Point to launch-facts and messaging.
- Don't write slides or talk tracks. A talk plan is a separate job, not
  this skill's.
