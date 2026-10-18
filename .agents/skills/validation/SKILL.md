---
name: validation
description: Validate PBIP/PBIR/TMDL edits or audit project structure, bindings, field references, rename cascades, and available native checks.
---

# Power BI Validation

Use this for PBIP/PBIR/TMDL edits or a requested project validation. Business
questions and page plans need their relevant semantic/planning review, not
structural commands against nonexistent or unchanged artifacts.

## Harness-neutral validation contract

The validator script lives in the intact module checkout. For an adopting
project, pass its explicit absolute path as `target`; `.` is only appropriate
when deliberately checking the module itself. Resolve the script using the
[module path contract](../../../docs/factory-module.md#paths-and-tools),
then run these steps in order:

1. `node /path/to/powerbi-module/workspace/engine/validate-pbip.mjs /absolute/project/target`;
2. `pbir validate /absolute/project/Report.Report --all` for each report when `pbir` is
   installed;
3. approved Fabric existence or item checks only when service scope is
   relevant.

For renames, also search affected model/report references for the old names,
including filters, sort definitions, DAX queries, and diagram layouts. A
missing optional tool or an unrun service check is not a completion claim.
Read the reported scope count: zero reports and models proves no project
structure. Unsupported `--changed` file types are reported as an unavailable
file check; use the containing project directory for structural validation.

When a change can affect a KPI, data shape/model, or access-sensitive decision,
use the [canonical regression recipe](../../../docs/validation.md#representative-data-domain-regressions)
and report the selected case, its result, or its evidence gap. Inspect actual
final bytes and affected documentation.

Return files changed, blockers, warnings, exact paths, commands run, unavailable checks, and
remaining risks. Native Power BI, Fabric, Tabular Editor, and DAX Studio
results are optional evidence and must never be invented. Return this handback
concisely at the caller's requested depth and language.

## Common blockers

- invalid JSON
- broken `definition.pbir` binding
- missing theme/resource files
- page/visual folder-name mismatch
- renamed fields still referenced in visuals
- TMDL indentation or malformed descriptions
