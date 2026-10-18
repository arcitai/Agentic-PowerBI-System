# Power BI for Factory

A Power BI domain module for [Factory](https://github.com/arcitai/factory),
maintained by [Arc’IT AI](https://github.com/arcitai).

Factory supplies the common Foundation, AgentOps and ADLC method. This module
adds the Power BI preparation, specialist skills and checks needed to make a
Power BI Factory: from a business question to a model and report you can verify.
It adds no separate orchestration service or mandatory application runtime.

| Part | What this module adds |
| --- | --- |
| [Power BI Foundation](.agents/skills/powerbi-foundation/SKILL.md) | Decision and KPI context, data/model ownership, project files, available tools, refresh/access boundaries and readiness evidence |
| [Power BI ADLC](.agents/skills/powerbi-adlc/SKILL.md) | Domain criteria and routing for specification, model/DAX/report work, review and authorized delivery |
| [Specialist skills](.agents/skills/README.md) | Power BI, PBIP/PBIR/TMDL, DAX, reports, Fabric, validation and domain audit |
| [Local checks](docs/validation.md) | A dependency-free PBIP/PBIR/TMDL validator and synthetic valid/invalid fixtures |

Factory continues to own general work admission, coordination and delivery
rules. The Power BI module supplies the specialist knowledge and proof.
ADLC means **Agentic Development Lifecycle**.

## Use the module

1. Adopt a reviewed Factory revision through its normal
   [Foundation route](https://github.com/arcitai/factory/tree/v0.1.18/foundation/factory-foundation).
2. Keep a reviewed checkout or extracted package of this module intact. Follow
   [module adoption](docs/factory-module.md); copying isolated skill files would
   lose their linked domain contracts and tools.
3. Use **Power BI Foundation** to assess the intended work against the adopting
   project's existing brief and environment. Reuse known context and evidence.
4. Use **Power BI ADLC** alongside the applicable Factory skills for an accepted
   task. Models come before reports when both need building; a page plan alone
   does not require a model or Desktop installation.
5. Keep outcomes and evidence in the adopting project's existing records.
   Module adoption does not require a second ledger in this repository.

```text
Factory core + Power BI preparation, skills and checks → Power BI Factory
business question → definitions and data → model → report → decision → proof
```

The module is a method and tool bundle, not an auto-installed Factory plugin.
The repository and npm identifiers remain `Agentic-PowerBI-System` and
`agentic-powerbi-system` for compatibility. Existing standalone users can keep
using the [legacy evidence route](.agents/skills/agentic-powerbi-system/SKILL.md)
and workspace described below; their records are not migrated or deleted.

## Verify this repository

```sh
npm run doctor
npm run validate
npm test
npm run audit -- --scope both
npm pack --dry-run
```

## Distinct assurance routes

- **Deterministic validation** runs mechanical PBIP/PBIR/TMDL and repository
  checks against a named target.
- **Power BI/domain audit** applies the `powerbi` contract to business meaning,
  model design, DAX, shaping risk, report storytelling, and ownership.
- **Semantic or visual review** uses specialist judgment or native tools to
  assess behavior that deterministic checks cannot prove.
- **Per-change Review** is the lifecycle gate for accepting a proposed change.
- **Periodic System audit** reads accumulated repository/workspace health,
  proves its live upstream relation, and returns `PASS`, `FAIL`, or `BLOCKED`
  without repair or durable audit artifacts.

Select the periodic scope explicitly:

```sh
npm run audit -- --scope repository
npm run audit -- --scope workspace
npm run audit -- --scope both
```

The audit uses current repository and workspace truth. It references the
existing domain-audit and validation contracts and does not require another
System implementation.

An approved Agentic Design System handoff can supply `DESIGN.md`, report
composition, tokens, and preview intent. Revalidate it against actual Power BI
capabilities, data, accessibility, and tenant constraints; the handoff is
reference input, not an execution requirement.

## Optional compatibility workspace

```text
workspace/
├── PROJECT-BRIEF.md       decision, KPI, data, and proof contract
├── briefs/                active bounded briefs
├── models/                active semantic-model work
├── reports/               active report work
├── state/                 local System state
├── runs/                  one durable evidence directory per route
├── history/runs.jsonl     append-only relation between runs
├── learning/              durable notes intentionally retained
└── engine/                optional local validators, tracer, and tests
examples/                  deliberately curated standalone proof
docs/                      contract and validation notes
```

The optional legacy `agentic-powerbi-system` route inspects prior records before routing work. It never copies
request transcripts into the ledger. A run is valid without promotion; a
curated example is written only when explicitly requested and includes its own
README and proof file.

## Safety

Require explicit authorization for deleting pages or visuals, rebinding reports,
changing `.platform` IDs, publishing, overwriting service items, or changing
RLS, refresh and access policy. Honor existing exact authorization; local edits
do not authorize protected identity or service changes. Keep tenant IDs,
credentials, connection strings, private data, and
generated local Power BI state out of Git and fixtures.

`npm pack --dry-run` runs a read-only seed guard. It succeeds for blank
placeholders and deliberate curated examples, and refuses to bundle mutable
workspace evidence without deleting or resetting it.

## Compatibility evidence-runner proof

Run the full local route in a disposable checkout or temporary copy:

```sh
python3 workspace/engine/tracer.py --promote-example
python3 workspace/engine/tracer.py --simulate-failure
python3 workspace/engine/tracer.py --recover --promote-example
```

The fixed demonstration clock makes the first clean run `run-0001`. The failed
run remains in the ledger, and the recovery run points to that predecessor.
The source repository should remain a seed with empty operational placeholders
after validation.

## License

MIT.
