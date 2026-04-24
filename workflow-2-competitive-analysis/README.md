# Workflow 2 — AI Engine Movement Alerts

**Category:** Competitive Analysis
**Stack:** Claude Desktop + Peec AI MCP server
**Built with:** #BuiltWithPeec

## What it does

Detects week-over-week shifts in how AI engines (ChatGPT, Gemini, Claude, AI Mode, Perplexity) talk about Linear vs Jira, Asana, ClickUp, Notion, Monday.com, and Trello — and surfaces them as Slack-ready alerts.

The signal is the **delta**, not the absolute number. Linear at 35% visibility on Claude is fine; Linear dropping from 35% → 22% on Claude in one week is a fire.

## Why it matters

Most marketing teams check their dashboards weekly, eyeball the number, and forget. By the time a competitor takes a citation source from you, you're 6 weeks behind. This workflow flips that: it tells you *the moment something shifts*, on *which engine*, and *because of which competitor or chat*.

Also works on a daily cadence — paste `/digest` into your morning Slack thread.

## Setup (3 minutes)

1. Install Claude Desktop and the Peec MCP server (see Workflow 1 README).
2. Create a Claude Desktop Project called "Linear — Competitive Movement Alerts".
3. Paste `system-prompt.md` into the project's Custom instructions.
4. Run `/snapshot` to confirm data flows, then `/digest` for the first real alert.

## Demo

```
/snapshot
/digest
/investigate best project management tool for engineering teams
/alert-rules
```

## How it uses Peec MCP

| Step | Peec tool | Purpose |
|---|---|---|
| Per-engine matrix | `get_brand_report` (dim=model_id) | Visibility/SoV broken down per engine |
| Period comparison | `get_brand_report` (date range) × 2 | Current 7d vs prior 7d delta |
| Chat-level investigation | `list_chats` + `get_chat` | Read actual AI responses driving the shift |
| Prompt resolution | `list_prompts` | Fuzzy-match user query to tracked prompt |

## Repeatability

Designed for daily or weekly cadence:
- **Daily:** `/digest` posted to Slack each morning by the marketing lead
- **Weekly:** `/snapshot` + `/digest` combined into the Monday standup deck
- **Ad-hoc:** `/investigate <prompt>` whenever a stakeholder asks "are we in the conversation for X?"

## Project link

https://app.peec.ai/projects/or_45c84dd8-183b-42ae-9598-1956575af925
