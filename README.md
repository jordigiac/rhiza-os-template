# Rhiza OS Template

The master template for the operating systems Rhiza Systems installs in client
businesses. One folder of plain markdown that an AI (Claude Code or Claude
Desktop) reads to act as the business's consultant and execution layer.

## How this repo is organized

```
rhiza-os-template/
├── template/    ← THE PRODUCT. Cloned once per client, then customized.
│                  Everything inside is client-facing, plain English.
└── playbook/    ← RHIZA-SIDE. Jordi's agendas, SOPs, and references.
                   Never copied into a client's install.
```

## How a client install works

1. Clone `template/` into a new private repo the client owns.
2. Run the onboarding interview live on a call (see
   `playbook/onboarding-call/`). It fills the knowledge files, sets the
   first automations, and deletes `setup/` when done.
3. Jordi builds connections, automations, and skills on retainer from there.

## Ground rules baked into the product

- Plain markdown and folder conventions only — works in any LLM tool.
- The client owns the repo and every credential. Keys live in `.env`,
  gitignored, never in any other file.
- The OS consults by default; the client decides; Jordi engineers.
- Automations graduate a trust ladder: human-checked beta → passes custom
  evals consistently → fully automated.

## Status (2026-08-02)

- Structure: built.
- `setup/ONBOARDING.md`: v1 draft — to be refined with Jordi before first
  client use.
- `.claude/skills/`: placeholder — the preset system-health skills (onboard,
  handoff, audit, level-up) get defined in the skills build session.
