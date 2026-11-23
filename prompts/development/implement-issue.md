# Execute: Implement a Specified Issue

## Objective

Implement the issue identified by the user in the current repository.

## Procedure

1. Resolve the target repository and issue number or URL. If either is ambiguous, ask one focused clarification.
2. Read repository instructions, contribution guidelines, architecture documentation, and the complete issue description, including acceptance criteria and discussion.
3. Inspect the relevant implementation and tests. Identify dependencies and the smallest complete solution.
4. If the issue is materially ambiguous or its requirements conflict with the existing architecture, explain the conflict and ask before making a consequential assumption.
5. Implement the requested behavior. Avoid unrelated refactoring and preserve compatibility unless the issue explicitly requires a breaking change.
6. Add or update automated tests for the behavior and relevant edge cases.
7. Run relevant tests, static analysis, formatting, and build checks. Report unavailable checks honestly.
8. Review the complete diff for correctness, security, secrets, accidental files, and scope creep.
9. Follow the repository's branch and release policy. Never bypass branch protections or required reviews. Do not merge or deploy without explicit authorization.
10. Commit or open a PR only when consistent with the repository workflow and the user's authorization. Do not close the issue until its acceptance criteria are met.

## Final report

Include the issue link, implementation summary, changed files, verification results, commit/PR link if applicable, and any remaining limitations.
