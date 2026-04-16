# 🤖 Agents

This folder documents custom GitHub Copilot agents—specialized chat modes defined as `.agent.md` files that give Copilot focused expertise and behavior for specific development tasks.

## Available Agents

### Recommended Agents from awesome-copilot

| Agent | Description |
|---|---|
| [C# Expert](https://github.com/github/awesome-copilot/blob/main/agents/CSharpExpert.agent.md) | Expert .NET developer agent for clean, secure, and maintainable C# code following SOLID principles, async patterns, and testing best practices |
| [.NET Upgrade](https://github.com/github/awesome-copilot/blob/main/agents/dotnet-upgrade.agent.md) | Perform janitorial tasks on C#/.NET code including cleanup, modernization, and tech debt remediation with structured per-project upgrade plans |

## How to Use Agents

**To Install:**

Download the `.agent.md` file and place it in your workspace under `.copilot/agents/`:

```bash
# Install C# Expert agent
curl -o .github/agents/CSharpExpert.agent.md https://raw.githubusercontent.com/github/awesome-copilot/main/agents/CSharpExpert.agent.md

# Install .NET Upgrade agent
curl -o .github/agents/dotnet-upgrade.agent.md https://raw.githubusercontent.com/github/awesome-copilot/main/agents/dotnet-upgrade.agent.md
```

**To Apply:**

- Agents appear as selectable modes in the GitHub Copilot Chat agent picker in VS Code
- Select the desired agent from the chat mode dropdown before starting a conversation
- Each agent applies its specialized system prompt and instructions for the duration of the session

## Discover More Agents

For additional agents, visit the [awesome-copilot agents repository](https://github.com/github/awesome-copilot/tree/main/agents) organized by:

- Languages (C#, Python, JavaScript, etc.)
- Frameworks and platforms (.NET, Azure, etc.)
- Development practices (upgrades, security, testing, etc.)

## Official Documentation

For more information on agents and custom chat modes:

- [About Custom Agents](https://docs.github.com/en/copilot/concepts/agents/copilot-cli/about-custom-agents)
- [GitHub Copilot Custom Chat Modes](https://docs.github.com/en/copilot/customizing-copilot/using-custom-chat-modes-in-github-copilot)
- [awesome-copilot Agents](https://github.com/github/awesome-copilot/tree/main/agents)
