# Power BI for Factory

Turn a business question into an owned, validated Power BI model, report, and
decision journey that can retain its operational proof across runs.

## Shared lifecycle

For an adopting project, Factory owns general Foundation, AgentOps and ADLC.
This module adds Power BI preparation and domain criteria; it does not copy
Factory or become another agent runtime. See [module adoption](docs/factory-module.md).

For maintenance of this repository, use the installed AIOS plugin (0.4.0 or later) for shared procedures:
`aios-spec-work`, `aios-build-work`, `aios-review-work` and `aios-ship-work`.
Spec owns conditional technology selection; Review owns generic repository
health audits. Resolve these skills through the harness, not copied files or
hardcoded cache paths. This repository owns its requirements, specialist
methods, checks, release facts and recovery. Keep those facts here and load
only the phase and local context needed for the change.

Work in the current task by default, including when opened directly from the
sidebar. Use `aios-orchestrate-workers` only for requested or concretely
beneficial delegation, or existing-worker recovery. Verify each selected root
and preserve one writer for overlapping changes. Repository work does not
preload personal AIOS context. Plugin availability is an authoring capability,
not a dependency of the product at runtime; if unavailable, report the method
gap and perform only work adequately covered by the local contract. Do not
recreate generic skills locally.

## Module contract

This repository is the Power BI domain module for Factory. The main routes are
`.agents/skills/powerbi-foundation/SKILL.md` for readiness and
`.agents/skills/powerbi-adlc/SKILL.md` for accepted Power BI work. The skill index
is `.agents/skills/README.md`. The adopting project owns its business brief,
models, reports and evidence; do not create a second mandatory ledger here.
Keep the module checkout intact so specialist references and validators resolve.

The existing `agentic-powerbi-system` route and `workspace/` seed remain an
optional compatibility workflow for existing users. Its append-only evidence,
failure/recovery and explicit example-promotion rules still apply when selected.
`examples/` holds deliberate proof and `docs/` holds the public contracts.
Do not put secrets, tenant identifiers, private data or generated local Power BI
state in this module's Git history or distributable package.

## Start

1. Read the adopting project’s existing brief and preserve resolved context.
   `workspace/PROJECT-BRIEF.md` supplies missing Power BI criteria; it is not a
   requirement to create a duplicate brief. Use it directly in the optional seed workflow.
2. For Power BI outcomes, resolve the relevant decision, audience, KPI definitions,
   data owners, refresh/runtime, proof, and optional design handoff from existing
   context. Repository maintenance does not require a new business brief.
3. When building a model/report outcome, model first: use a star schema,
   explicit relationships, hidden technical keys, and explicit measures.
4. Report second: one page per business question, with the decision and its
   evidence ahead of decoration.
5. Validate every PBIP/PBIR/TMDL edit and record unavailable optional tools.

## Specialist routes

- `.agents/skills/powerbi-foundation/SKILL.md`: Power BI readiness and preparation
- `.agents/skills/powerbi-adlc/SKILL.md`: domain routing within Factory ADLC
- `.agents/skills/powerbi/SKILL.md`: business question, decision, KPI, and
  audit framing
- `.agents/skills/pbip/SKILL.md`: PBIP/PBIR/TMDL structure and safe edits
- `.agents/skills/dax/SKILL.md`: measures and semantic logic
- `.agents/skills/report/SKILL.md`: page plans, states, visuals, and filters
- `.agents/skills/fabric/SKILL.md`: service and Fabric work under authority
  gates
- `.agents/skills/validation/SKILL.md`: deterministic completion proof
- `.agents/skills/system-audit/SKILL.md`: read-only periodic accumulated-state
  health

The specialist skills are harness-neutral contracts. The deterministic doctor,
PBIP validator, Python System engine, and tests live under
`workspace/engine/` and are callable directly or through the package scripts.
Normal `npm pack`/publish packaging also runs the read-only seed guard; mutable
workspace evidence causes an explicit failure and is never removed.

## Rules

- Keep KPI name, DAX, format, interpretation, limitation, and business owner
  together.
- Use deterministic validation before visual inspection or guesses.
- Keep deterministic validation, Power BI/domain audit, semantic or visual
  review, per-change Review, and periodic System audit as distinct routes.
- Preserve data ownership, row-level security, refresh, workspace, and publish
  authority boundaries.
- Require explicit authorization for deleting pages or visuals, rebinding
  reports, changing `.platform` IDs, publishing, overwriting service items, or
  changing RLS/access/refresh policy. Honor existing exact authorization;
  local editing scope does not authorize protected identity or service changes.
- Do not invent PBIX/PBIP evidence or require optional Power BI tools that are
  unavailable.
- Finish with changed files, validation evidence, unavailable checks, and
  remaining risk.

## Proof

```sh
node workspace/engine/doctor.mjs
node workspace/engine/validate-pbip.mjs . --ignore-tests
npm test
python3 workspace/engine/system_audit.py --scope both
npm pack --dry-run
```

Use `pbir validate`, Fabric CLI, Tabular Editor, DAX Studio, Power BI Desktop,
or `pbi-tools` only when the command is truthfully installed and the project
scope justifies it. Record exact unavailable checks rather than inferring
their result.
