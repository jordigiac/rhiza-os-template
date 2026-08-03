# [Automation or skill name] — dataset

The test cases this build is graded on. Two sources: **real examples the
owner labeled** (the gold standard) and **synthetic cases** generated to
cover situations the real examples miss — always realistic inputs grounded
in this business's actual constraints.

| # | Input | What good looks like | Source | Holdout? |
|---|---|---|---|---|
| 1 | [the real message / file / situation] | [the owner's own judgment] | owner-labeled | no |
| 2 | [a generated edge case] | [expected handling] | synthetic | yes |

Rules:

- **Holdouts stay locked.** Cases marked holdout are never used while
  iterating — only for the final graduation run. That's how we know the
  build learned the job, not the test.
- **Escaped failures join forever.** Any failure that happens in a real run
  becomes a new case here, so it can never silently come back.
