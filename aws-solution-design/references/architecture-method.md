# Architecture decision method and quality gate

## Decision method

Apply this method proportionally to the request.

1. **Frame the decision.** Express the business outcome, stakeholders, scope, constraints, decision horizon, measurable quality attributes, and consequences of doing nothing. Convert vague goals such as “highly available” into measurable targets or explicitly marked assumptions.
2. **Characterize the workload.** Capture traffic shape, data volume and sensitivity, latency, consistency, availability, RPO/RTO, integration, geography, compliance, growth, operational model, skills, and dependencies.
3. **Identify hard gates.** Eliminate options that cannot meet residency, regulatory, security, latency, compatibility, quota, timeline, or organizational constraints. Flag facts needing current AWS verification.
4. **Generate viable options.** Include the status quo and non-AWS/hybrid choices only when credible. Prefer the smallest set that exposes the meaningful tradeoff; avoid ceremonial alternatives.
5. **Evaluate consistently.** Compare options against functional fit, security, reliability, performance, operability, delivery risk, team fit, cost, sustainability, lock-in, and reversibility. Weight criteria when consequential; explain scoring and uncertainty rather than using false precision.
6. **Recommend and expose consequences.** State why the option wins, what it makes harder, residual risks, assumptions, prerequisites, and conditions that would change the choice.
7. **Validate.** Use prototypes, measurements, threat modeling, quota checks, cost models, Well-Architected review, failure testing, and stakeholder review according to risk. Record evidence and gaps.
8. **Record and revisit.** Add the decision to the log with an owner, status, consequences, and concrete revisit triggers such as scale, price, regulation, team capability, or service availability changes.

## AWS Well-Architected coverage

Use the six pillars as a review lens, not as a checkbox exercise:

- **Operational Excellence:** ownership, organization, automation, safe change, observability, runbooks, incident learning, readiness, and improvement.
- **Security:** identity foundation, traceability, layered protection, data protection, automated controls, preparedness, and minimizing direct human data access.
- **Reliability:** foundations and quotas, resilient architecture, consistent change, failure management, backups, recovery objectives, and tested recovery.
- **Performance Efficiency:** workload-appropriate choices, measurement, evolution, scaling, managed options, and explicit tradeoffs.
- **Cost Optimization:** financial ownership, consumption model, unit economics, waste removal, demand/supply matching, and attributed cost.
- **Sustainability:** utilization, efficient software/data patterns, managed services, lifecycle choices, and demand alignment.

For each relevant pillar, name the requirement or risk, chosen response, validation evidence, remaining gap, owner, and priority. Do not claim alignment solely because an AWS service is used.

## Cross-cutting analysis prompts

- **IAM and security:** Who or what can perform each sensitive action? How is identity established, scoped, reviewed, revoked, and audited? What are the trust boundaries and abuse paths? What happens if a credential, workload, account, region, or dependency is compromised?
- **Networking:** Where does traffic enter, exit, route, resolve names, cross boundaries, and fail over? Are IP space, bandwidth, latency, quotas, asymmetric routing, and private service access understood?
- **Resilience and DR:** Which failures are absorbed, which degrade service, and which require recovery? Are RTO/RPO business-approved and supported by dependencies? Can restore, failover, and failback be proven?
- **Data:** Who owns the data and schema? What consistency, integrity, lifecycle, sovereignty, deletion, backup, replication, and reconciliation guarantees are required?
- **Integration:** Are contracts versioned and observable? Are timeouts, retries, idempotency, ordering, duplicates, poison messages, backpressure, and partial failure handled?
- **Operations:** Can operators detect customer impact, find the cause, act safely, and learn from incidents? Are alerts actionable and routine changes automated?
- **Cost and performance:** Which assumptions drive capacity and cost? What happens at peak and under growth? Are transfer, observability, backups, support, licenses, DR, and idle environments included?
- **Delivery and migration:** How is the target introduced safely? How are data correctness, coexistence, rollback, blast radius, and decommissioning validated?

## Quality gate before delivery

Confirm that the document:

- leads with a plain-language recommendation and business outcome;
- distinguishes facts, assumptions, estimates, open questions, and decisions;
- traces critical requirements to components, controls, risks, and tests;
- defines important acronyms and explains concepts before technical detail;
- covers all relevant template chapters and explains genuine non-applicability;
- specifies identity, trust boundaries, data flows, failure behavior, ownership, and operational responsibilities;
- states measurable availability, recovery, security, performance, and cost assumptions where material;
- compares credible alternatives with explicit tradeoffs and avoids unsupported certainty;
- considers every AWS Well-Architected pillar and records gaps or accepted risks;
- includes migration/deployment, rollback, testing, evidence, risks, dependencies, next actions, and a decision log;
- identifies AWS facts needing current validation, including regional availability, quotas, pricing, limits, and compliance eligibility;
- does not expose secrets, recommend broad IAM permissions without justification, or treat backups as proven until restore testing is defined.

If a critical gate fails because information is unavailable, surface it prominently as a blocker, assumption, or pre-implementation validation item.
