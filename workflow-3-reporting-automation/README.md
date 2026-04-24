# Workflow 3 — Monthly Executive AI-Visibility Brief

**Category:** Reporting Automation
**Stack:** Claude Desktop + Peec AI MCP server
**Built with:** #BuiltWithPeec

## What it does

Replaces 4 hours of analyst work with a single command. Generates a board-ready, one-page monthly brief on Linear's AI-search performance — visibility trend, share of voice by engine, sentiment, top winners/losers, citation sources, and recommended actions — in clean markdown ready to paste into Notion, Google Docs, or an email.

## Why it matters

Marketing leaders need a recurring artifact for leadership reviews. Building it manually means: pulling numbers, calculating month-over-month deltas, ranking prompts, cross-referencing citation gaps, prioritizing actions, then writing prose. Every month. This workflow does all of it in one prompt.

## Setup (3 minutes)

1. Install Claude Desktop and the Peec MCP server (see Workflow 1 README).
2. Create a Claude Desktop Project called "Linear — Monthly Exec Brief".
3. Paste `system-prompt.md` into the project's Custom instructions.
4. On the 1st of each month, run `/exec-brief` and paste the output into your monthly leadership doc.

## Demo

```
/exec-brief
/section 4
/email-version
```

## How it uses Peec MCP

| Step | Peec tool | Purpose |
|---|---|---|
| Headline numbers | `get_brand_report` (×2 date ranges) | This month vs prior month deltas |
| Per-engine table | `get_brand_report` (dim=model_id) | Engine-level breakdown |
| Winning prompts | `get_brand_report` (dim=prompt_id, sorted desc) | Top 5 prompts where Linear wins |
| Losing prompts | `get_brand_report` (dim=prompt_id, sorted asc) | Top 5 prompts where Linear loses |
| Citation sources | `get_domain_report` | Top 5 domains feeding the AI |
| Actions | `get_actions` (scope=overview) | Recommended next steps |
| Name resolution | `list_brands`, `list_prompts` | Convert IDs to readable names |

## Repeatability

This is the textbook reporting-automation workflow:
- **Monthly:** `/exec-brief` on the 1st of each month
- **Iterative:** `/section <n>` to refresh just one part if data updates mid-cycle
- **Distribution:** `/email-version` to hand to comms or send directly to the CEO

The system prompt enforces a strict, repeatable output structure so briefs are directly comparable month over month.

## Project link

https://app.peec.ai/projects/or_45c84dd8-183b-42ae-9598-1956575af925
