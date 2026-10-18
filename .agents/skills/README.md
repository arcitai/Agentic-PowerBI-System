# Power BI module skill shelf

This module owns Power BI-specific methods and tools. Factory owns the general
Foundation, AgentOps and ADLC method. An adopting project owns its product
rules, business context and evidence. Keep the module's linked files together;
see [adoption](../../docs/factory-module.md).

Each direct skill uses `.agents/skills/<name>/SKILL.md`; folder and frontmatter
names agree. The two module entry points add domain criteria, not copied
Factory procedures. Existing specialist and compatibility routes stay available.

## Skill index

- `.agents/skills/powerbi-foundation/SKILL.md`: Power BI readiness and preparation
  for the intended project work.
- `.agents/skills/powerbi-adlc/SKILL.md`: Power BI criteria and specialist routing
  within the adopting project's Factory ADLC.
- `.agents/skills/agentic-powerbi-system/SKILL.md`: optional legacy route for prior-run
  inspection, specialist routing, and durable proof.
- `.agents/skills/powerbi/SKILL.md`: business questions, decisions, KPI
  contracts, and Power BI domain audit.
- `.agents/skills/pbip/SKILL.md`: safe PBIP, PBIR, and TMDL structure and edits.
- `.agents/skills/dax/SKILL.md`: explicit measures and semantic logic.
- `.agents/skills/report/SKILL.md`: report pages, states, visuals, filters, and
  layout.
- `.agents/skills/fabric/SKILL.md`: authority-gated Fabric and Power BI Service
  work.
- `.agents/skills/validation/SKILL.md`: deterministic local and optional native
  completion proof.
- `.agents/skills/system-audit/SKILL.md`: read-only periodic evaluation of
  accumulated repository and workspace health.

Validate this shelf directly with
`python3 workspace/engine/checks.py --skills-only`.

Factory supplies the generic lifecycle in adopting projects. This repository
uses its installed AIOS procedures for repository maintenance. Neither needs
a second lead or worker merely to read a specialist skill. Domain checks add
criteria to the selected lifecycle; they do not replace its acceptance rules.
