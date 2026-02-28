# Claude Code Best Practices

**Type:** Knowledge Base / CLI Templates  
**Repo:** [shanraisshan/claude-code-best-practice](https://github.com/shanraisshan/claude-code-best-practice)  
**Stars:** ~2.5k (as of Feb 2026)

## Overview

Comprehensive collection of best practices, configurations, and templates for Claude Code. Covers skills, agents, memory, rules, hooks, MCP servers, plugins, and marketplaces.

## Key Concepts

| Concept | Purpose | Location |
|---------|---------|----------|
| **Skills** | Reusable knowledge, workflows, slash commands | `.claude/skills/` |
| **Agents** | Custom agents with own tools/permissions/model | `.claude/agents/` |
| **Memory** | Persistent context via CLAUDE.md & `@path` | `CLAUDE.md` files |
| **Rules** | Modular topic-specific instructions | `.claude/rules/*.md` |
| **Hooks** | Deterministic scripts on events | `.claude/hooks/` |
| **MCP Servers** | Model Context Protocol integrations | External servers |
| **Plugins** | Bundled packages (skills + agents + hooks + MCP) | Distributed via Marketplace |
| **Marketplaces** | Discover/install plugins | `code.claude.com/plugins` |
| **Sandboxing** | File/network isolation | Built-in runtime |
| **Output Styles** | Configurable response tone/format | `settings.json` |

## Why This Repo?

- ✅ **Stay updated** — tracks changes in Claude Code features
- ✅ **Templates** — ready-to-use skills, agents, rules
- ✅ **Best practices** — security, performance, maintainability
- ✅ **Community-driven** — reflects real-world usage patterns

## Installation

No installation required. Clone the repo and cherry-pick what you need:

```bash
git clone https://github.com/shanraisshan/claude-code-best-practice.git
cp -r .claude/skills/ ~/.claude/
```

## Usage

1. Browse categories in the repo
2. Copy relevant files to your `.claude/` directory
3. Restart Claude Code
4. Skills become available as `/skill-name` commands

## Example: Custom Agent

```yaml
# .claude/agents/my-agent.json
{
  "name": "SeniorReviewer",
  "color": "#FF6B6B",
  "model": "claude-3-7-sonnet",
  "tools": ["file_read", "file_write", "shell"],
  "instructions": "Review code for security and performance"
}
```

## Rating

**9/10** — essential reference for Claude Code power users.

## Links

- **Docs:** https://code.claude.com/docs
- **Marketplace:** https://code.claude.com/plugins
- **MCP Spec:** https://github.com/modelcontextprotocol/specification