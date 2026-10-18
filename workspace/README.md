# Optional compatibility workspace

`workspace/` is the existing Agentic Power BI System seed and evidence flow.
It remains available to standalone users. New Factory module work uses the
adopting project’s existing brief and evidence instead; see
[module adoption](../docs/factory-module.md). No records are migrated or deleted.

- `PROJECT-BRIEF.md` is the active decision, KPI, data, security, refresh, and
  publish contract.
- `briefs/` holds additional bounded briefs when a project needs them.
- `models/` and `reports/` hold active semantic-model and report work.
- `state/` holds only safe, local System state; generated Power BI cache remains
  excluded.
- `runs/` holds durable evidence for each route attempt.
- `history/runs.jsonl` keeps the append-only relation between runs.
- `learning/` holds durable notes intentionally retained for future work.
- `engine/` contains optional local validators, the deterministic tracer, and
  dependency-light tests.

Run records keep references to input, output, and proof artifacts instead of
copying request transcripts into the ledger. No service, database, or external
System installation is needed to understand this workspace.
