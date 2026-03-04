# Hyperbot Skills

> Hyperbot MCP (Model Context Protocol) 服务器的 AI 智能体技能集合。

## 简介

Hyperbot Skills 帮助 AI 智能体（如 Cursor、Claude）有效地安装和使用 Hyperbot MCP 服务器。它提供了结构化知识，包括如何连接 MCP 服务器、配置凭据，以及使用每个可用工具进行聪明钱分析、鲸鱼追踪、市场数据查询、交易者统计和仓位分析。

## Claude/Cursor skills vs OpenClaw skills

**Claude/Cursor skills** = 用户安装 skill → 智能体用它来**为用户设置 MCP**并调用工具。**OpenClaw skills** = 机器人获取 skill 页面 → 机器人**自主安装和使用** MCP。

## OpenClaw Skill URL

对于 OpenClaw 机器人，使用以下 skill URL：

```
https://clawhub.ai/developHyperbotNetwork/hyperbot-mcp
```

## 什么是 Skills？

Skills 是结构化的知识文件，为 AI 编码智能体提供特定领域的专业知识。它们遵循可在不同 AI 工具间通用的可移植格式。当你安装一个 skill 后，智能体将学会如何安装 hyperbot-mcp-server，以及如何使用每个 MCP 工具进行加密货币交易分析，而无需搜索外部文档。

## 可用 Skills

| Skill | 描述 |
|-------|-------------|
| **hyperbot-mcp-skill** | 安装并使用 Hyperbot MCP — 聪明钱排行榜、鲸鱼监控、市场数据、K 线图、交易者统计、仓位分析。涵盖连接、凭据配置以及所有用于加密货币交易分析的 MCP 工具。 |

## 安装

### 快速安装（推荐）

```bash
npx skills add developHyperbotNetwork/hyperbot-skills
```

全局安装（所有项目可用）：

```bash
npx skills add developHyperbotNetwork/hyperbot-skills -g
```

### 手动安装（Cursor / Claude）

**个人 skill**（所有项目可用）：

```bash
git clone https://github.com/developHyperbotNetwork/hyperbot-skills.git
cp -r hyperbot-skills/skills/* ~/.cursor/skills/
```

**项目 skill**（仅当前项目）：

```bash
git clone https://github.com/developHyperbotNetwork/hyperbot-skills.git
cp -r hyperbot-skills/skills/* .cursor/skills/
```

### 使用 skill

安装后，当你要求以下操作时，智能体将使用该 skill：

- 安装或连接 Hyperbot MCP 服务器
- 分析聪明钱地址及其交易策略
- 追踪鲸鱼持仓并监控大额交易
- 获取实时市场数据、K 线图和订单簿信息
- 查询交易者统计并评估交易表现
- 分析仓位历史和 PnL 数据
- 生成市场情绪分析和交易建议

示例提示词：

- "如何在 Cursor 中安装 hyperbot-skills？"
- "展示本周胜率最高的聪明钱交易者"
- "鲸鱼现在对 BTC 在做什么？"
- "获取 ETH 最新 15 分钟周期的 K 线数据"
- "分析这个交易者的表现：0x..."
- "基于订单簿数据，当前市场情绪如何？"
- "找出过去 7 天高 ROI 的聪明钱地址"

## Skill 结构

```
hyperbot-skills/
├── skills/
│   └── hyperbot-mcp-skill/
│       ├── SKILL.md                    # 主要技能：安装 + 工具使用
│       └── references/
│           └── prompts-reference.md    # MCP 分析提示词
└── README.md
```

## 参考资料

- **官方网站:** https://hyperbot.network
- **Hyperbot MCP Server GitHub 仓库:** https://github.com/developHyperbotNetwork/hyperbot-skills
