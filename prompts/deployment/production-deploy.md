# Execute: Production Deployment

## Objective

Prepare and, when explicitly authorized, execute a production deployment for the target application.

## Safety gate

A production deployment is a consequential action. First establish the target repository, production environment, release commit, deployment method, and rollback path.

If the user has not explicitly authorized execution of this deployment, perform the preparation and verification steps, then stop before changing production.

## Procedure

1. Read repository deployment instructions and identify the documented production workflow.
2. Confirm the target environment and release commit. Never infer that a development or staging environment is production.
3. Inspect CI status, required reviews, branch protections, release notes, migrations, dependency changes, and outstanding blockers.
4. Check backup and rollback readiness, including database migration reversibility where relevant.
5. Identify expected downtime, queue/worker effects, scheduled tasks, storage changes, and external service dependencies.
6. Present a concise pre-deployment checklist and stop for authorization if it has not already been granted.
7. After authorization, execute only the documented deployment process. Do not bypass CI, approvals, or repository policies.
8. Verify deployment health using available health checks, logs, smoke tests, and critical user flows.
9. If verification fails, follow the documented rollback or mitigation procedure. Do not improvise destructive recovery steps.
10. Report the exact release commit, deployment outcome, verification evidence, and any remaining risks.

## Constraints

- Never expose secrets.
- Never run destructive database or infrastructure operations without explicit, specific authorization.
- Never claim success based solely on a deployment command returning successfully.
- If the rollback path is unknown or unsafe, stop and report that before deployment.

## Final report

Include target environment, release commit, preflight checks, actions performed, health verification, rollback status if applicable, and unresolved issues.
