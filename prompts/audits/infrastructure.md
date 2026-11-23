# Execute: Repository Infrastructure Audit

## Objective

Audit the infrastructure and engineering setup of the current repository and produce a prioritized, evidence-based report.

## Scope

Inspect applicable areas, including:

- Runtime and language versions.
- Framework and major dependency versions.
- Dependency health, outdated packages, and known deprecations.
- Application configuration and environment-variable handling.
- Build tooling and asset pipeline.
- Automated tests, static analysis, formatting, and quality gates.
- CI workflows, caching, artifacts, and deployment automation.
- Hosting, containers, process management, queues, schedulers, and workers where present.
- Database migrations, backups, storage, and operational recovery.
- Logging, monitoring, error reporting, and health checks.
- Security controls, secrets handling, permissions, and dependency risk.
- Documentation and developer onboarding.

Adapt the scope to the actual stack. Do not assume technologies are present.

## Procedure

1. Confirm the repository and inspect its instructions and architecture.
2. Inventory relevant configuration and workflow files.
3. Inspect actual versions and configuration rather than relying only on README claims.
4. Run safe, read-only checks where available. Do not upgrade dependencies, change configuration, deploy, or mutate infrastructure during an audit.
5. Separate verified facts, inferred risks, and items that could not be checked.
6. Identify concrete issues with evidence, impact, likelihood, and remediation.
7. Prioritize recommendations by severity and practical value. Identify dependencies between recommendations.

## Final report

Include:
- Executive summary and overall assessment.
- Repository and stack inventory.
- Findings grouped by critical/high/medium/low priority.
- Evidence and affected files/configuration for each finding.
- Recommended remediation steps.
- Quick wins versus larger improvements.
- Checks performed and checks unavailable.

Do not claim a security certification or comprehensive assurance from a repository-only review. Explicitly identify areas requiring access to live infrastructure.
