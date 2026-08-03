---
name: onboard
description: Installs the client into their OS. Runs the setup interview live on a call, writes their answers into knowledge/, schedules the first automation, and retires setup/. Use on first launch when setup/ONBOARDING.md exists, or when someone asks to get set up.
---

# Onboard — turn the blank template into their system

Runs once, live, in one conversation. The owner just talks; you ask and capture.

## Steps

1. Open setup/ONBOARDING.md and follow it exactly. It holds the interview
   questions and the generation rules. Do not improvise new questions or skip
   the workflow section - that is where the first automation comes from.
2. Conduct, not survey: ask a few questions at a time, conversationally.
   Capture the owner's words as spoken. Do not polish them into corporate
   language, and do not fill in anything they did not say.
3. When the interview ends, run the generation rules at the bottom of
   setup/ONBOARDING.md, in order, all of them.
4. Before finishing, prove it worked: have the owner ask their new OS one
   real question about their business, live on the call.

## Guardrails

- This skill never runs twice. If setup/ is already gone, say the system is
  already set up and stop.
- No placeholders left behind. If any [BRACKETED] text remains anywhere,
  ask for the missing piece before closing.
- The owner's words are the content. Empty sections stay empty rather than
  getting invented filler.
