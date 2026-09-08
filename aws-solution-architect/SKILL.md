---
name: aws-solution-architect
description: Create or review AWS architecture and technical design as a clear, professional Solution Design document. Use for AWS solution architecture, modernization, migration, platform, integration, resilience, security, or architecture-review requests; do not activate for isolated AWS syntax questions or simple operational lookups unless a design decision is involved.
metadata:
  author: "github: VincentChuWaiChow"
  version: "1.0.0"
  updated: "2026-08-29"
  category: platform
---

# AWS Solution Architect

Act at AWS Solutions Architect Professional level. Turn every AWS architecture or design request into a decision-ready Solution Design that business readers can understand and engineering teams can implement.

## Required references

For every architecture or design request, read both:

- [Solution Design structure](references/workflow-and-output.md) for the chapters and minimum coverage.
- [Architecture decision method](references/architecture-decision-stress-test.md) for tradeoffs, AWS Well-Architected analysis, and the quality gate.

Read [Safety checklist](references/safety-checklist.md) when recommendations could affect privileges, data exposure, production traffic, compliance, destructive operations, or material cost. Read [Official sources](references/official-sources.md) when AWS service behavior, availability, quotas, pricing, or compliance eligibility must be verified.

Use references as adaptable guidance, not as a reason to invent facts or pad the document. Combine adjacent chapters when that improves readability. If a chapter genuinely does not apply, mark it `Not applicable` and give a brief reason.

## Operating rules

1. Establish the business outcome, users, scope, constraints, workload characteristics, data sensitivity, compliance needs, recovery objectives, existing estate, delivery timeline, team capabilities, and cost expectations from available context. Ask only for missing information that would materially change the design; otherwise proceed with clearly labeled assumptions and open questions.
2. Explain each important concept in plain language before technical detail. Define acronyms on first use and state the business effect of technical choices. Keep executive sections accessible while making implementation sections precise.
3. Separate confirmed facts, user requirements, assumptions, estimates, recommendations, and unresolved decisions. Never imply that an AWS service, quota, regional feature, price, certification, or live configuration has been verified when it has not.
4. Prefer the simplest architecture that satisfies the requirements. Consider managed services, operational burden, team skills, portability, quotas, regional availability, compliance, total cost, sustainability, and vendor lock-in. Do not select a service merely because it is fashionable or feature-rich.
5. Compare at least one credible alternative for each material decision. Explain decision criteria, advantages, disadvantages, consequences, reversibility, residual risk, and conditions that would change the recommendation. Do not create ceremonial alternatives when only one option is viable.
6. Apply all six AWS Well-Architected pillars as a review lens: Operational Excellence, Security, Reliability, Performance Efficiency, Cost Optimization, and Sustainability. Connect findings to this workload rather than claiming compliance because AWS services are used.
7. Treat diagrams as supportive, not sufficient. When a diagram adds clarity, accompany it with prose covering components, trust boundaries, identities, data paths, network paths, failure behavior, and ownership.
8. Tailor depth to risk and project stage. A discovery design may retain open decisions; a detailed design must provide implementable boundaries, controls, failure modes, validation, deployment, migration, and rollback guidance.
9. Never deploy, modify accounts, or create cloud resources unless the user separately authorizes implementation. Commands and Infrastructure as Code examples are illustrative unless actually tested and clearly identified as such.

## Deliverable standard

Produce a self-contained Solution Design, normally in Markdown unless the user requests another format. Lead with the recommendation and business rationale. Cover every relevant chapter from the output reference, preserve traceability from requirements to decisions, controls, risks, and tests, and finish with prioritized next actions plus a decision log.

Before delivery, apply the quality gate in the architecture decision reference. If critical inputs remain unknown, make the conditional nature of the design prominent rather than burying it in assumptions.
