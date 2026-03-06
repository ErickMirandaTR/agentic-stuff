# 🛠️ Agent Skills

This folder contains a curated collection of agent skills for GitHub Copilot—both local custom skills and recommended skills from the awesome-copilot repository.

## Available Skills

### Local Skills

| Skill | Description |
|---|---|
| [develop-pr](./develop-pr/) | Create a develop PR when the user provides a user story number and a branch name |
| [release-pr](./release-pr/) | Create release and develop PRs when given a user story number, branch name, and release branch |

### Recommended Skills from awesome-copilot & skills.sh

| Skill | Description |
|---|---|
| [blazor-expert](https://skills.sh/markpitt/claude-skills/blazor-expert) | Comprehensive Blazor development expertise covering Blazor Server, WebAssembly, and Hybrid apps |
| [web-design-guidelines](https://skills.sh/vercel-labs/agent-skills/web-design-guidelines) | Review UI code for Web Interface Guidelines compliance and accessibility standards |
| [excalidraw-diagram-generator](https://github.com/github/awesome-copilot/tree/main/skills/excalidraw-diagram-generator) | Generate Excalidraw diagrams from natural language descriptions for flowcharts, architecture, and mind maps |

## How to Install Skills

### Install Local Skills

To install a local skill from this repository:

```bash
npx skills add https://github.com/ErickMirandaTR/agentic-stuff/tree/main/skills --skill <skill-name>
```

**Examples:**

```bash
# Install develop-pr skill
npx skills add https://github.com/ErickMirandaTR/agentic-stuff/tree/main/skills --skill develop-pr

# Install release-pr skill
npx skills add https://github.com/ErickMirandaTR/agentic-stuff/tree/main/skills --skill release-pr
```

### Install Skills from awesome-copilot

To install skills from the awesome-copilot repository:

```bash
npx skills add https://github.com/github/awesome-copilot/tree/main/skills --skill <skill-name>
```

**Example:**

```bash
# Install excalidraw-diagram-generator skill
npx skills add https://github.com/github/awesome-copilot/tree/main/skills --skill excalidraw-diagram-generator
```

### Install Skills from skills.sh

For skills hosted on [skills.sh](https://skills.sh), visit the skill's page directly and follow the installation instructions provided.

## Evaluating Skills

Before installing any skill, especially from third-party sources, it's recommended to review its quality and security:

- **skills.sh Audit Information**: Each skill on [skills.sh](https://skills.sh) includes an audit report that shows:
  - Code quality metrics
  - Security assessments
  - Functionality validation
  - Author information and reputation
  
- **Evaluation Checklist**:
  - ✅ Review the skill's audit/quality report
  - ✅ Check the skill description and use cases
  - ✅ Verify the author and community feedback
  - ✅ Review any open issues or concerns
  - ✅ Test the skill in a sandbox environment first
  - ✅ Check if it requires any special permissions or API keys

- **awesome-copilot Skills**: These are curated by GitHub and generally follow strict quality standards, but it's still good practice to review documentation before installation.

⚠️ **Warning**: Only install skills from trusted sources and review their audit information before adding them to your development environment.

## Discover More Skills

For additional skills beyond these recommendations, explore:

- [awesome-copilot skills repository](https://github.com/github/awesome-copilot/tree/main/skills)
- [skills.sh](https://skills.sh)

## Official Documentation

For more information on agent skills and how they work:

- [Agent Skills Specification](https://agentskills.io/specification)
- [GitHub Copilot Skills Documentation](https://docs.github.com/en/copilot/using-github-copilot/using-copilot-extensions-and-tools)
- [awesome-copilot Repository](https://github.com/github/awesome-copilot)
