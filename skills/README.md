# Skills

This folder contains local skills you can install and use with the `npx skills` CLI.

| Skill | Description | Install Command | Spec |
|---|---|---|---|
| `develop-pr` | Create a develop PR when the user provides a user story number and a branch name. | `npx skills add https://github.com/ErickMirandaTR/agentic-stuff/tree/main/skills --skill develop-pr` | `skills/develop-pr/SKILL.md` |
| `release-pr` | Create release and develop PRs when given a user story number, branch name, and release branch. | `npx skills add https://github.com/ErickMirandaTR/agentic-stuff/tree/main/skills --skill release-pr` | `skills/release-pr/SKILL.md` |

| Optional Command | Purpose |
|---|---|
| `npx skills list` | List installed skills (if supported by your CLI version). |
