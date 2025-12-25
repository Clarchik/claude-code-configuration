# Clarchik's Claude Code Marketplace

A personal Claude Code marketplace configuration for productive modern web development.

## Overview

This plugin provides a curated set of commands and MCP servers designed to enhance your Claude Code experience for web development workflows.

## Features

### Custom Commands

This plugin includes three productivity-focused commands:

### 📋 Development Commands (7)

- `/code-explain` - Generate detailed explanations
- `/code-optimize` - Performance optimization
- `/code-cleanup` - Refactoring and cleanup

### MCP Servers

This plugin includes 2 pre-configured MCP servers:

#### **Context7** (`@upstash/context7-mcp`)
Access up-to-date, version-specific documentation for any library.

**Benefits:**
- Always current documentation
- Version-specific information
- Works with thousands of libraries
- No manual searching required

#### **Playwright** (`@playwright/mcp`)
Browser automation and web testing capabilities.

**Use Cases:**
- E2E testing
- Web scraping
- Browser automation
- Visual testing
- Screenshot capture

## Installation

### From GitHub (Recommended)

```bash
# Add marketplace
/plugin marketplace add clarchik/claude-code-configuration

# Install plugin
/plugin install claude-code-configuration
```

### From Local Clone (for development)

```bash
git clone https://github.com/clarchik/claude-code-configuration.git
cd claude-code-configuration

# Add as local marketplace
/plugin marketplace add ./

# Install plugin
/plugin install claude-code-configuration
```

### Option 2: Install from Source

```bash
git clone https://github.com/clarchik/clarchik-claude-marketplace.git
cd clarchik-claude-marketplace
claude-code plugin install ./
```

## Usage

After installation, restart Claude Code to activate the plugin.

### Using Commands

Commands can be invoked using the `/` prefix:

```bash
/code-explain #filePath
/code-optimize #filePath
/code-cleanup #filePath
```

### Using MCP Servers

MCP servers are automatically available after installation. Simply reference them in your prompts:

```
"Use context7 to find the latest React documentation"
"Use playwright to take a screenshot of example.com"
```

## Configuration

You can customize settings by creating a `.claude/settings.local.json` file:

```json
{
  "statusLine": {
    "type": "command",
    "command": "/path/to/your/statusline",
    "padding": 0
  },
  "alwaysThinkingEnabled": false
}
```

## Requirements

- Claude Code CLI
- Node.js and npx (for MCP servers)
- Internet connection (for MCP server downloads)

## Tags

- `productivity` - Enhance your development workflow
- `typescript` - TypeScript-focused development
- `api` - API development support
- `development` - General development tools
- `mcp` - Model Context Protocol integration

## License

MIT License - See [LICENSE](./LICENSE) for details.

## Author

**Clarchik**
- GitHub: [https://github.com/clarchik](https://github.com/clarchik)

## Support

For issues, questions, or contributions, please visit the [GitHub repository](https://github.com/clarchik/clarchik-claude-marketplace).

## Learn More

- [Claude Code Documentation](https://docs.claude.com/en/docs/claude-code)
- [MCP Documentation](https://modelcontextprotocol.io)
- [MCP Server Directory](https://mcpcat.io)
