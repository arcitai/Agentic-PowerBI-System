---
name: powerbi-adlc
description: Apply Power BI domain criteria and specialist skills within an accepted Factory development task, from definition and file work to review and authorized delivery.
---

# Power BI ADLC

Use alongside the applicable Factory ADLC skill for accepted Power BI work.
Factory retains the general specification, implementation, independent review,
evaluation and delivery rules. AgentOps retains coordination and the owner's
mandate. This module supplies domain criteria, not another generic lifecycle.

Read the adopting project's accepted task, current brief and relevant prior
evidence. Use [Power BI Foundation](../powerbi-foundation/SKILL.md) only for a
preparation gap that affects this task. Keep resolved choices and use the
project's existing artifact/evidence locations; do not require a ledger in the
module checkout.

## Select the domain work

| Need in the accepted task | Specialist and required result |
| --- | --- |
| Business decision, KPI definition or domain audit | [powerbi](../powerbi/SKILL.md): decision, audience, grain, meaning, owner and bounded assumptions |
| Project structure, model bindings or file edits | [pbip](../pbip/SKILL.md): valid PBIP/PBIR/TMDL structure and complete reference changes |
| Measures and semantic logic | [dax](../dax/SKILL.md): explicit measure, format, interpretation and representative semantic checks |
| Pages, visuals and report states | [report](../report/SKILL.md): one decision per page, evidence, filters, accessible and mobile states |
| Authorized Fabric/service operation | [fabric](../fabric/SKILL.md): exact operation, target, authorization, observed result and recovery |
| File completion or requested structural validation | [validation](../validation/SKILL.md): deterministic target checks first, plus available relevant native proof |

Use only the rows relevant to the work. For model/report builds, establish the
model before the report. A page-plan request can finish with a reviewed plan;
it does not require manufacturing a model, executing all rows or installing
Power BI Desktop.

## Apply the checks in the owning lifecycle

The task specification records the business decision, affected domain objects,
acceptance evidence and exact authority. Keep KPI name, DAX, format,
interpretation, limitation and owner together. Do not guess unknown data,
refresh, access or service facts.

Implement through the selected specialists and verify at the nearest useful
domain boundary. A changed KPI, grain, relationship or access-sensitive result
needs the [representative regression](../../../docs/validation.md#representative-data-domain-regressions)
that demonstrates its intended effect. Valid file syntax cannot prove totals,
visual usefulness, RLS enforcement or a live refresh.

Independent review uses the actual candidate and affected proof, including
unavailable checks. Retain Factory's delivery decision and existing exact
delegation. Local file authority does not grant publishing, rebinding, deleting
report assets, changing `.platform` identity, RLS, access or refresh policy;
follow the [data-change boundary](../../../docs/contract.md#data-change-boundary).
Stop only the dependent operation when its authority or required proof is absent.

Return the changed artifacts, domain outcome, evidence, unavailable checks and
remaining risk to the existing Factory task. Leave project evidence with its
owner. The [legacy evidence runner](../agentic-powerbi-system/SKILL.md) is used
only when an existing standalone workspace explicitly selects that flow; it is
not a prerequisite or a second acceptance gate for this module.
