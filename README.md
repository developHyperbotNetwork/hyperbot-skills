[中文](README_zh.md) | [English](README.md)

# Hyperbot Skills

> Hyperbot MCP (Model Context Protocol) AI Agent skills collection.

## Introduction

Hyperbot Skills helps AI agents (such as Cursor, Claude) effectively install and use the Hyperbot MCP server. It provides structured knowledge, including how to connect to the MCP server, configure credentials, and use each available tool for smart money analysis, whale tracking, market data queries, trader statistics, and position analysis.

## Claude/Cursor skills vs OpenClaw skills

**Claude/Cursor skills** = User installs skill → Agent uses it to **set up MCP for the user** and call tools. **OpenClaw skills** = Bot fetches skill page → Bot **autonomously installs and uses** MCP.

## OpenClaw Skill URL

For OpenClaw bots, use the following skill URL:

```
https://clawhub.ai/developHyperbotNetwork/hyperbot-mcp
```

## What are Skills?

Skills are structured knowledge files that provide AI coding agents with domain-specific expertise. They follow a portable format that can be used across different AI tools. When you install a skill, the agent learns how to install hyperbot-mcp-server and how to use each MCP tool for cryptocurrency trading analysis without searching external documentation.

## Available Skills

| Skill | Description |
|-------|-------------|
| **hyperbot-mcp-skill** | Install and use Hyperbot MCP — Smart money leaderboard, whale monitoring, market data, K-line charts, trader statistics, position analysis. Covers connection, credential configuration, and all MCP tools for cryptocurrency trading analysis. |

## Installation

### Quick Installation (Recommended)

```bash
npx skills add developHyperbotNetwork/hyperbot-skills
```

Global installation (available for all projects):

```bash
npx skills add developHyperbotNetwork/hyperbot-skills -g
```

### Manual Installation (Cursor / Claude)

**Personal skill** (available for all projects):

```bash
git clone https://github.com/developHyperbotNetwork/hyperbot-skills.git
cp -r hyperbot-skills/skills/* ~/.cursor/skills/
```

**Project skill** (only for current project):

```bash
git clone https://github.com/developHyperbotNetwork/hyperbot-skills.git
cp -r hyperbot-skills/skills/* .cursor/skills/
```

### Using the skill

After installation, when you request the following actions, the agent will use the skill:

- Install or connect to Hyperbot MCP server
- Analyze smart money addresses and their trading strategies
- Track whale positions and monitor large transactions
- Get real-time market data, K-line charts, and order book information
- Query trader statistics and evaluate trading performance
- Analyze position history and PnL data
- Generate market sentiment analysis and trading recommendations

Example prompts:

- "How to install hyperbot-skills in Cursor?"
- "Show the smart money traders with highest win rate this week"
- "What are whales doing with BTC right now?"
- "Get ETH latest 15-minute interval K-line data"
- "Analyze this trader's performance: 0x..."
- "Based on order book data, what is the current market sentiment?"
- "Find smart money addresses with high ROI in the last 7 days"

## Skill Structure

```
hyperbot-skills/
├── skills/
│   └── hyperbot-mcp-skill/
│       ├── SKILL.md                    # Main skill: Installation + Tool usage
│       └── references/
│           └── prompts-reference.md    # MCP analysis prompts
└── README.md
```

## References

- **Official Website:** https://hyperbot.network
- **Hyperbot MCP Server GitHub Repository:** https://github.com/developHyperbotNetwork/hyperbot-skills
