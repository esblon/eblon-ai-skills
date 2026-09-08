# Official AWS sources and grounding

Use authoritative, current AWS sources when a recommendation depends on service behavior, regional availability, quotas, pricing, support, or compliance eligibility. Prefer specific service documentation over summaries.

## Starting points

- AWS Well-Architected Framework: https://docs.aws.amazon.com/wellarchitected/latest/framework/welcome.html
- AWS Architecture Center: https://aws.amazon.com/architecture/
- AWS service documentation: https://docs.aws.amazon.com/
- AWS Regional Services: https://aws.amazon.com/about-aws/global-infrastructure/regional-product-services/
- Service Quotas: https://docs.aws.amazon.com/servicequotas/latest/userguide/intro.html
- AWS Pricing: https://aws.amazon.com/pricing/
- AWS Compliance Programs: https://aws.amazon.com/compliance/programs/

## Grounding rules

- Official documentation explains AWS behavior; it does not prove the user's live account, Region, quota, configuration, entitlement, price, or compliance state.
- Prefer read-only live evidence when the user has provided an appropriate connection. Otherwise use repository evidence, sanitized user-provided evidence, or official documentation and label the evidence level.
- Never invent account identifiers, Amazon Resource Names (ARNs), resource names, quotas, prices, certifications, or live configuration.
- Cite sources near claims when source attribution is requested or when a time-sensitive fact materially affects the design.
- Record the date and Region for time-sensitive checks. Identify any fact that must be revalidated before implementation.
