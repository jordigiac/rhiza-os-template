# [Automation or skill name] — scorers

What "done" looks like, written so it can be tested. Vague criteria are
useless ("should be accurate"); testable ones name the check ("cites the
source file; invents nothing").

Every scorer returns PASS or FAIL plus a one-line critique.

| Scorer | Type | Pass condition |
|---|---|---|
| [format-check] | code | [e.g., output has all six fields, under 200 words] |
| [judgment-check] | judge | [rubric: e.g., priority matches how the owner labeled similar cases] |

Judge scorers get a short rubric written here, with one or two example
critiques so the judge grades consistently.

**Graduation bar:** [e.g., 90% of cases pass AND every holdout passes] —
set when this eval is created, changed only with a note here saying why.

Scorecards from each run land in `scorecards/`, dated, never edited after
the fact. Each scorecard records the pass rate, the baseline it was compared
against, and case-by-case results — an average can hide a regression on the
case that matters most.
