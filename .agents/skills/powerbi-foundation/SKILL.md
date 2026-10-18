---
name: powerbi-foundation
description: Prepare or assess the Power BI-specific context, files, tools and operational boundaries needed by a Factory project.
---

# Power BI Foundation

Use when adopting this module or when a Power BI readiness gap affects accepted
work. Factory Foundation owns generic host/repository preparation; this skill
adds the Power BI criteria. Assessment is read-only. Setup authority covers only
the requested preparation, not changes to data, access, refresh or service items.

## Scope the preparation

Identify the adopting project, intended outcome and existing brief. Reuse its
resolved business context and records. The module's
[brief](../../../workspace/PROJECT-BRIEF.md) supplies missing domain questions;
do not create a second brief or run ledger just to use the module.

Resolve only what the intended work needs:

| Work | Required domain preparation |
| --- | --- |
| Business question or page plan | Decision, audience, KPI meanings, source references, assumptions and proof of usefulness |
| Model, DAX or report-file changes | Project paths, data ownership and grain, model/report bindings, affected measures, representative inputs and a working validator |
| Native model/report review | The actual authorized Desktop, Tabular Editor, DAX or report tools and a representative check; package presence is not proof |
| Refresh, RLS or service delivery | Exact tenant/workspace/item boundary, data and access owner, operation authority, applicable native tools, verification and recovery |

Missing Desktop or service access does not block an authorized page plan or
local file validation. It does prevent claims about visual rendering, live DAX,
refresh, RLS enforcement or publishing that require those capabilities.

## Inspect the project and tools

For file work, inspect the existing PBIP/PBIR/TMDL structure and bindings using
[PBIP](../pbip/SKILL.md). Preserve `.platform` identity and `.pbi` local state.
Use the [validation contract](../validation/SKILL.md) on the actual target.
Commands and links resolve relative to the intact module checkout as described
in [adoption](../../../docs/factory-module.md#paths-and-tools).

Check optional native tools only when needed for this task. Record unavailable
tools rather than installing, signing in or changing workspace access without
the necessary authority. No customer data, connection secrets or tenant IDs
belong in the module's distributed seed.

## Hand back readiness

Return each relevant capability as **verified**, **required gap**, or
**conditional/not needed**, with its observed evidence and owner/next action.
Record the result in the adopting project's existing record. A successful local
validator proves file checks only; a tool on PATH does not prove a working native
or service journey. AgentOps can continue authorized work on ready capabilities
and return affected gaps to Foundation.

Once work is accepted and ready, use [Power BI ADLC](../powerbi-adlc/SKILL.md)
alongside the selected Factory skills. Do not repeat generic admission or
delivery gates here.
