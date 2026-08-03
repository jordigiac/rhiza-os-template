# Rhiza OS Template

The master template for the operating systems Rhiza Systems installs in client
businesses. One folder of plain markdown that an AI (Claude Code or Claude
Desktop) reads to act as the business's consultant and execution layer.

## How this repo is organized

```
rhiza-os-template/
└── template/    ← THE PRODUCT. Cloned once per client, then customized.
                   Everything inside is client-facing, plain English.
```

This repo carries the product only. Jordi's agendas and playbooks live in
Rhiza's Notion (Internal Documents → Agendas / Playbooks), and the
workspace-shapes reference lives in the Rhiza OS knowledge folder.

## How a client install works

1. Clone `template/` into a new private repo the client owns.
2. Run the onboarding interview live on a call (agenda and checklist live in
   Rhiza's Notion). It fills the knowledge files, sets the first automations,
   stamps the install, and deletes `setup/` when done.
3. Jordi builds connections, automations, and skills on retainer from there.

## Ground rules baked into the product

- Plain markdown and folder conventions only — works in any LLM tool.
- The client owns the repo and every credential. Keys live in `.env`,
  gitignored, never in any other file.
- The OS consults by default; the client decides; Jordi engineers.
- Automations graduate a trust ladder: human-checked beta → passes custom
  evals consistently → fully automated.

## Status (2026-08-03)

- Structure: built.
- Three preset skills live: onboard, handoff, audit. There is no level-up
  skill — its questions live in the monthly call agenda in Notion.
- `setup/ONBOARDING.md`: v1 draft — refined at the client-lifecycle pass
  before first client use.
- Meeting agendas and playbooks: published to Notion 2026-08-03; this repo
  is product-only.
