# Execute: Next Repository Issue

## Objective

Identify the next appropriate open issue in the current repository, implement it, verify the result, and report what happened.

## Procedure

1. Establish the target repository from the current project, conversation, connected GitHub context, or explicitly supplied URL. If multiple repositories are plausible, ask which one.
2. Read the repository's contribution guide, agent instructions, development documentation, and relevant architecture notes before changing code.
3. Inspect open issues. Consider labels, priority, dependencies, blockers, scope, and whether an issue is already being handled. Do not select a blocked issue when a suitable unblocked issue exists.
4. Select one issue and explain briefly why it is the next appropriate task.
5. Read the issue and inspect the relevant code before proposing an implementation.
6. Implement the issue with the smallest coherent change that satisfies its acceptance criteria. Preserve established conventions and avoid unrelated refactoring.
7. Add or update tests where appropriate. Run the relevant test suite, static analysis, formatting, and build checks available in the repository.
8. Inspect the final diff for accidental changes, secrets, debug code, generated files, and regressions.
9. Follow the repository's current branch and release policy. Do not bypass required reviews, branch protections, or CI. Do not merge a pull request or deploy unless explicitly authorized.
10. If the repository's documented workflow permits direct commits to its active development branch, commit only after checks pass. Otherwise, use the required branch/PR workflow.
11. Update or close the issue only when the work genuinely satisfies its acceptance criteria and the available permissions and workflow allow it. Never close an issue merely because implementation has started.

## Constraints

- Do not invent issue requirements or claim tests passed when they were not run.
- Do not make destructive changes or modify production systems without explicit authorization.
- If blocked by missing access, credentials, ambiguous requirements, or failing unrelated infrastructure, stop at the safe boundary and report the blocker.
- Do not ask for information that can be established from the repository or issue.

## Final report

Include:
- Selected issue number, title, and link.
- Why it was selected.
- Summary of implementation.
- Files or areas changed.
- Tests and checks run, with actual outcomes.
- Commit and PR links, if created.
- Issue status.
- Remaining risks or blockers.
