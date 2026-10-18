# Adopt the Power BI module

The module composes with Factory's Foundation, AgentOps and ADLC responsibilities.
It adds Power BI-specific preparation, methods and validators. It does not add
an execution runtime, service, global plugin registry or a second work queue.

## Responsibilities

| Owner | Responsibility |
| --- | --- |
| Factory core | General project/host readiness, coordination, task lifecycle and delivery decisions |
| Power BI Foundation | Domain readiness: business/KPI context, project files, tools, data/access/refresh boundaries |
| Power BI ADLC and specialists | Domain implementation criteria, model/DAX/report work and truthful completion evidence |
| Adopting project | Product rules, business data, brief, model/report artifacts, access and evidence |

A **Power BI Factory** is the core method plus this domain module and the
project's qualified tools. The term does not imply that Desktop, Fabric or an
autonomous hosted service is bundled or already qualified.

## Select and retain the sources

1. Adopt Factory through its existing
   [Foundation guidance](https://github.com/arcitai/factory/tree/v0.1.18/foundation/factory-foundation).
   This module is aligned with Factory 0.1.18's three responsibilities; that
   source mapping is not a claim of a live, unattended installation.
2. Keep a reviewed version of this complete repository or its extracted npm
   package in a separate tools directory. Record the exact revision and location
   in the adopting project's existing tool/adoption record.
3. Make these entry points available through the selected harness's supported
   skill/reference mechanism:
   - `.agents/skills/powerbi-foundation/SKILL.md`
   - `.agents/skills/powerbi-adlc/SKILL.md`
4. Verify that the harness can read the selected entry points, their linked
   specialists and supporting files. Do not copy isolated `SKILL.md` files into
   a global skill directory: references and tools depend on the intact module.
   This change neither configures a harness nor claims native skill discovery.

Keep customer data and operational evidence in the adopting project. Resolve
missing domain details using `workspace/PROJECT-BRIEF.md` as a checklist, without
overwriting the project's brief or making every optional service field mandatory.

## Paths and tools

`module_root` means the reviewed module directory containing `package.json`,
`.agents/skills/`, `docs/` and `workspace/engine/`. All relative tool paths in
specialist skills are relative to that module directory, not the customer repo.
Pass an absolute path to the authorized Power BI project:

```sh
node /path/to/powerbi-module/workspace/engine/doctor.mjs
node /path/to/powerbi-module/workspace/engine/validate-pbip.mjs /path/to/report-project
```

The validator operates on its explicit target. Review its diagnostics and exit
status; a missing target is not a successful empty validation. The module's own
`npm run validate` checks this repository and deliberately ignores test fixtures.
It is not the command for validating a customer project.
`--changed <file>` requires an existing file; after a deletion, validate the
containing project directory so references are checked in context.
The scan prints its report/model count; zero objects does not prove a customer
project was checked. Unsupported changed-file types produce a warning (exit 1).

Node.js 20+ and Python 3.9+ support the existing local checks. Power BI Desktop,
Tabular Editor, DAX tooling, `pbir` and Fabric tools are selected according to the
task and actual platform. Their absence remains a named evidence gap where
required; it does not block an unrelated plan or local file check.

## Example: a margin-report task

The project already has an approved margin definition and a model. Foundation
checks the affected sources, model/report paths, validator and intended proof;
it does not repeat host setup that is still qualified. Power BI ADLC selects
DAX and PBIP work for the accepted measure change, then the relevant validation
and representative input/filter checks. Report review confirms the decision
journey where a suitable native tool exists. Publishing remains conditional on
the exact workspace/item authority and service proof. The Factory task keeps
one specification, review result and delivery decision.

For a page-plan-only request, select the business and report methods and review
that plan. Do not require Desktop, a ledger, a fake report file or publish access.

## Compatibility and updates

The GitHub repository name, npm name, CLI paths and existing specialist names
remain stable. `agentic-powerbi-system`, the tracer and `workspace/` evidence
format are optional compatibility facilities for existing users; records stay
append-only and are never silently migrated or deleted. `system-audit` audits
that selected repository/workspace; it does not automatically audit an unrelated
adopting project.

Keep Factory and the module independently pinned. To update, review the changed
domain contracts/tools, retain local project adaptations, and repeat affected
checks. To recover, return to the previous reviewed module revision and tooling;
do not reset project data or evidence. No module or core release is performed by
adding these instructions.
