# Agent Prompt Architect

> [繁體中文](./README.zh-TW.md)

A skill that teaches AI coding assistants how to generate well-structured agent system prompts using the CO-STAR framework.

This is a **skill** — a set of instructions that, once installed, gives your AI assistant the expertise to help you write better agent prompts interactively.

## How It Works

1. Copy `skill/SKILL.md` into your AI tool's skill/rules directory
2. Ask your AI assistant: "Help me write a system prompt for my agent"
3. The assistant follows the skill — interviews you, applies CO-STAR, generates prompt

## Installation

```bash
npx skills add paul0728/agent-prompt-architect
```

Or manually copy the `skill/` directory into your AI tool's skills location:

| Tool | Destination |
|------|-------------|
| Kiro | `.kiro/skills/agent-prompt-architect/` |
| Claude Code | `.claude/skills/agent-prompt-architect/` |
| Cursor | `.cursor/skills/agent-prompt-architect/` |
| GitHub Copilot | `.github/skills/agent-prompt-architect/` |
| Cline | `.cline/skills/agent-prompt-architect/` |
| Windsurf | `.windsurf/skills/agent-prompt-architect/` |

## What the Skill Teaches

Once installed, your AI assistant gains the ability to:

1. **Interview you** — Asks about your agent's role, tools, constraints, and output format
2. **Apply CO-STAR framework** — Structures the prompt with Context, Objective, Style, Tools, Anti-patterns, Response, Examples
3. **Generate few-shot examples** — Creates ✅/❌ pairs instead of verbose rules
4. **Run a quality checklist** — Verifies no hardcoded values, no conflicting rules, correct output format
5. **Handle multi-agent projects** — Recommends file organization and per-agent conventions

## CO-STAR Framework

| Section | Purpose |
|---------|---------|
| **C**ontext | Runtime variables (time, timezone) — injected dynamically |
| **O**bjective | Agent's role and primary goal |
| **S**tyle | Behavioral rules (when to call tools vs. respond with text) |
| **T**ools | Available tools with descriptions |
| **A**nti-patterns | Explicit "DO NOT" rules with correct/incorrect examples |
| **R**esponse | Output format specification |
| + **Examples** | 2-3 concrete input→output pairs |

## Architecture Support

The skill knows how to write prompts for:

- **ReAct agents** — Tool-calling loops with reasoning
- **Plan-then-Execute agents** — Planner + sequential executor
- **Summary / post-processing agents** — Report generation from tool outputs
- **Multi-agent orchestrators** — Routing and aggregation

## License

MIT
