# Hyperbot Skills

> A collection of AI agent skills for the Hyperbot MCP (Model Context Protocol) server.

## Introduction

Hyperbot Skills helps AI agents (e.g. Cursor, Claude) install and use the Hyperbot MCP server effectively. It provides structured knowledge on how to connect the MCP server, configure credentials, and use each available tool for smart money analysis, whale tracking, market data, trader statistics, and position analysis.

## Claude/Cursor skills vs OpenClaw skills

**Claude/Cursor skills** = user installs skill → agent uses it to **set MCP for the user** and call tools. **OpenClaw skills** = bot fetches the skill page → bot **installs and uses** MCP autonomously.

## OpenClaw Skill URL

For OpenClaw bots, use the following skill URL:

```
https://clawhub.ai/developHyperbotNetwork/hyperbot-mcp
```

## What are Skills?

Skills are structured knowledge files that give AI coding agents domain-specific expertise. They follow a portable format that works across different AI tools. When you install a skill, the agent learns how to install hyperbot-mcp-server and how to use each MCP tool for cryptocurrency trading analysis without needing to search external docs.

## Available Skills

| Skill | Description |
|-------|-------------|
| **hyperbot-mcp-skill** | Install and use Hyperbot MCP — smart money leaderboard, whale monitoring, market data, K-lines, trader statistics, position analysis. Covers connection, credentials, and every MCP tool for crypto trading analysis. |

## Installation

### Quick Install (Recommended)

```bash
npx skills add developHyperbotNetwork/hyperbot-skills
```

Install globally (available across all projects):

```bash
npx skills add developHyperbotNetwork/hyperbot-skills -g
```

### Manual Install (Cursor / Claude)

**Personal skill** (available across all projects):

```bash
git clone https://github.com/developHyperbotNetwork/hyperbot-skills.git
cp -r hyperbot-skills/skills/* ~/.cursor/skills/
```

**Project skill** (current project only):

```bash
git clone https://github.com/developHyperbotNetwork/hyperbot-skills.git
cp -r hyperbot-skills/skills/* .cursor/skills/
```

### Using the skill

Once installed, the agent will use the skill when you ask to:

- Install or connect Hyperbot MCP server
- Analyze smart money addresses and their trading strategies
- Track whale positions and monitor large transactions
- Get real-time market data, K-lines, and order book information
- Query trader statistics and evaluate trading performance
- Analyze position history and PnL data
- Generate market sentiment analysis and trading recommendations

Example prompts:

- "How do I install hyperbot-skills in Cursor?"
- "Show me the top smart money traders by win rate this week"
- "What are the whales doing with BTC right now?"
- "Get the latest K-line data for ETH with 15m interval"
- "Analyze this trader's performance: 0x..."
- "What's the current market sentiment based on order book data?"
- "Find smart money addresses with high ROI in the last 7 days"

## Skill Structure

```
hyperbot-skills/
├── skills/
│   └── hyperbot-mcp-skill/
│       ├── SKILL.md                    # Main skill: install + tool usage
│       └── references/
│           └── prompts-reference.md    # MCP prompts for analysis
└── README.md
```

## References

- **main website:** https://hyperbot.network
- **Hyperbot MCP Server GitHub repo:** https://github.com/developHyperbotNetwork/hyperbot-skills
