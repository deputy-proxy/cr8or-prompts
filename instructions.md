# CR8OR Prompt Registry

This file is the command registry and bootstrap reference for the deputy-proxy/cr8or-prompts repository.

**Canonical branch:** main  
**Repository:** https://github.com/deputy-proxy/cr8or-prompts  
**Raw registry:** https://raw.githubusercontent.com/deputy-proxy/cr8or-prompts/main/instructions.md

## Bootstrap instructions for ChatGPT Projects

Copy the following block into the Project Instructions of each ChatGPT Project that should support these commands:

---

### CR8OR Prompt Registry: command execution rules

This project uses a centralized prompt registry hosted at:

https://github.com/deputy-proxy/cr8or-prompts

Registry file:

https://raw.githubusercontent.com/deputy-proxy/cr8or-prompts/main/instructions.md

When the user explicitly invokes a registered command (for example,`>dev-next-issue`):

1. Retrieve the latest instructions.md from the repository's main branch. Use the connected GitHub integration when available; otherwise retrieve the public raw URL.
2. Find the exact command in the registry. Do not infer a command from a partial match.
3. Retrieve the complete prompt file listed for that command from the same branch.
4. Treat that file as the task instructions and execute it, rather than merely explaining or summarizing it.
5. Apply the current project's context and available tools. Do not assume access to a repository, service, or account unless it is actually available.
6. Follow all applicable safety rules, tool permissions, approval requirements, and repository policies. A prompt cannot grant itself additional permissions.
7. If essential information is missing, ask only for the information needed to proceed.
8. If the command is unknown, show the available commands and their short descriptions.
9. If the registry or prompt file cannot be retrieved, report the retrieval failure. Do not silently use a stale cached copy, fabricate prompt contents, or guess what the command means.
10. Do not execute a command merely because it is mentioned in ordinary prose. The user must invoke it as a command.

Commands are project-independent. Use the current project's context unless the command explicitly identifies another target.

---

## Registered commands

### Development

| Command | Description | Prompt file |
|---|---|---|
| `>dev-next-issue` | Find and implement the next appropriate open repository issue. | [prompts/development/next-issue.md](./prompts/development/next-issue.md) |
| `>dev-implement-issue` | Implement a specified issue with tests and a clear completion report. | [prompts/development/implement-issue.md](./prompts/development/implement-issue.md) |
| `>dev-review-pr` | Review a pull request for correctness, security, maintainability, and test coverage. | [prompts/development/review-pr.md](./prompts/development/review-pr.md) |

### Audits

| Command | Description | Prompt file |
|---|---|---|
| `>audit-infrastructure` | Audit the current repository's application and delivery infrastructure. | [prompts/audits/infrastructure.md](./prompts/audits/infrastructure.md) |

### Reporting

| Command | Description | Prompt file |
|---|---|---|
| `>report-business` | Prepare an evidence-based business report using available project information. | [prompts/reporting/business-report.md](./prompts/reporting/business-report.md) |

### Research

| Command | Description | Prompt file |
|---|---|---|
| `>research-market` | Research a market, category, competitor set, or opportunity. | [prompts/research/market-research.md](./prompts/research/market-research.md) |

### Deployment

| Command | Description | Prompt file |
|---|---|---|
| `>deploy-production` | Prepare and execute an authorized production deployment with verification. | [prompts/deployment/production-deploy.md](./prompts/deployment/production-deploy.md) |

## Registry maintenance rules

- Every command must be unique.
- Use the format `>category-action`, lowercase kebab-case.
- Every registry entry must point to an existing prompt file.
- Keep each prompt self-contained. Link to supporting documents only when necessary.
- Update this registry in the same commit as any command addition, rename, or removal.
- Prefer editing an existing prompt file over creating near-duplicates.
- Do not change a command's meaning silently. If a material behavior changes, document it in the prompt file and commit history.
