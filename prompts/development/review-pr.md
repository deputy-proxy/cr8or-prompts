# Execute: Review a Pull Request

## Objective

Perform a careful, evidence-based review of the specified pull request. Review only; do not modify repository files.

## Procedure

1. Resolve the repository and PR number or URL. Ask if ambiguous.
2. Read repository guidance and the PR description, linked issue, changed files, and full diff.
3. Inspect surrounding code and relevant call sites. Do not review the diff in isolation when behavior depends on broader context.
4. Evaluate correctness, regressions, security, data integrity, performance, accessibility where relevant, maintainability, and test coverage.
5. Check whether tests meaningfully cover the changed behavior. Run read-only or non-destructive checks if useful and permitted.
6. Report only actionable findings supported by evidence. For each finding include severity, file and line, the failure scenario, and a concrete suggested correction.
7. Distinguish confirmed defects from questions, risks, and style preferences. Do not report speculative concerns as bugs.
8. Do not approve, request changes, merge, or post comments unless the user explicitly asks you to submit a review and the relevant permissions are available.

## Final report

Start with one of: **Changes requested**, **No blocking findings**, or **Unable to complete**.

Then provide:
- Findings ordered by severity, with file/line references.
- Test and validation results.
- Important residual risks or review limitations.

If no actionable findings exist, say so clearly. Do not invent findings to make the review look substantial.
