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

## How a client install works (async-first, lifecycle v2 — 2026-08-08)

1. Payment lands → clone `template/` into a new private repo, seed
   `knowledge/problem-list.md` from the sales-call audit, and transfer the
   repo to the client's GitHub account. The welcome email carries
   `setup/START-HERE.md` and the bootstrap Loom (production materials —
   the Loom script and welcome emails — live in the Rhiza OS
   `workspaces/` folder, not in this repo).
2. The client installs alone, at their pace: claim the repo, clone via
   GitHub Desktop, install Claude, say hey. `setup/ONBOARDING.md` runs
   itself — machine check, interview, persona, contract — and finishes by
   pointing at the workshop booking. Nobody is on the other end; the
   setup sheet carries the stuck-line.
3. The workshop (60 min, live): install review, the API-key connections,
   then the first jam — first solution ships within the week.
4. Jordi maintains and expands on retainer from there; the monthly audit
   is the heartbeat.

## Ground rules baked into the product

- Plain markdown and folder conventions only — works in any LLM tool.
- The client owns the repo and every credential. Keys live in `.env`,
  gitignored, never in any other file.
- The OS consults by default; the client decides; Jordi engineers.
- Automations graduate a trust ladder: human-checked beta → passes custom
  evals consistently → fully automated.

## Status (2026-08-07)

- Structure: built. Five preset skills: onboard, handoff, checkup, audit,
  humanizer. There is no level-up skill — its questions live in the monthly
  call agenda in Notion.
- The OS has a self since 2026-08-06: PERSONA.md (woken at onboarding),
  CONTRACT.md (five starter laws, grows by the owner's spoken word),
  archive/ (boxed, never deleted), the teach phrases, corrections-teach-
  twice, self-healing connections, and the cost ladder.
- `setup/ONBOARDING.md`: v1.2 — machine setup baked in (Part 0); sandbox
  re-test in progress before client #1.
- Meeting agendas and playbooks: published to Notion 2026-08-03; this repo
  is product-only.
