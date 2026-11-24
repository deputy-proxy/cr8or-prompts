# CR8OR Prompts

A centralized, version-controlled prompt registry for reusable workflows across ChatGPT Projects and other AI tools.

**Repository:** https://github.com/deputy-proxy/cr8or-prompts  
**Default branch:** main  
**Registry:** [instructions.md](./instructions.md)

## How it works

1. Keep reusable prompts in this repository.
2. Add the bootstrap instructions from instructions.md to each ChatGPT Project's Project Instructions.
3. Invoke a registered command in a project chat, for example, `>dev-next-issue`.
4. The assistant reads the latest registry from main, retrieves the referenced prompt file, and executes it.

The registry is the source of truth. Project Instructions should contain only the bootstrap rules, not copies of individual prompts.

## Repository layout

- instructions.md: command registry and Project Instructions bootstrap.
- prompts/development/: development workflows.
- prompts/audits/: audit workflows.
- prompts/reporting/: reporting workflows.
- prompts/research/: research workflows.
- prompts/deployment/: deployment workflows.

## Adding a prompt

1. Create a Markdown file under the appropriate prompts/ directory.
2. Add a command entry to instructions.md with its name, description, and exact file path.
3. Keep commands unique and use lowercase kebab-case after the asterisk.
4. Commit both the prompt and registry update to main.

## Updating a prompt

Edit its Markdown file and commit the change. The next command invocation should retrieve the current version from GitHub. No copies in individual Projects need to be edited.

## Important operating notes

- The assistant must retrieve the registry and prompt file at invocation time; it must not assume a previously read copy is current.
- If GitHub access or retrieval fails, the assistant must report that and must not silently execute an old or guessed version.
- Prompts are instructions, not additional permissions. Existing tool permissions, safety requirements, repository policies, and user approvals still apply.
- Public raw registry URL: https://raw.githubusercontent.com/deputy-proxy/cr8or-prompts/main/instructions.md
- This is a prompt convention, not a native ChatGPT slash-command or automatic project-file synchronization feature. Execution depends on Project Instructions and the assistant's ability to retrieve repository content.
