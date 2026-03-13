# 🔌 MCP Servers

This folder contains documentation for Model Context Protocol (MCP) servers integrated with this workspace.

## What are MCP Servers?

MCP (Model Context Protocol) servers extend Copilot's capabilities by providing access to external tools, data sources, and services. They enable Copilot to interact with specialized systems and integrate domain-specific knowledge.

## Available MCP Servers

| Server | Description | Status |
|---|---|---|
| [Saffron](https://github.com/tr/a208070_ask_saffron_mcp-server/blob/feature/remote_mcp/README_test_mcp.md) | Saffron MCP server for specialized queries | Active |
| [GitHub](https://docs.github.com/en/copilot/how-tos/provide-context/use-mcp/use-the-github-mcp-server) | GitHub MCP server for repository and issue management integration | Active |
| [Azure DevOps](https://github.com/tr/aiplatform_mcp/tree/main/src/ado-mcp-server) | Azure DevOps MCP server for work item and project management | Active |

## How to Install and Configure MCP Servers

### Installation Steps

1. Identify the MCP server you want to use
2. Add the server configuration to your workspace settings
3. Configure any required environment variables or authentication
4. Verify the connection and test functionality

### Configuration Example

Add your MCP server configuration in your workspace or user settings:

```json
{
  "mcpServers": {
    "server-name": {
      "url": "http://localhost:3000",
      "type": "http",
      "headers": {
        "Authorization": "Bearer YOUR_API_TOKEN"
      }
    }
  }
}
```

## Resources

- [MCP Protocol Specification](https://modelcontextprotocol.io/docs)
- [Community MCP Server Examples](https://github.com/modelcontextprotocol/servers)
- [Copilot MCP Integration Guide](https://docs.github.com/en/copilot)
