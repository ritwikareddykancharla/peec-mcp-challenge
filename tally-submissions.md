# Tally Submission Descriptions

Three submissions, one per category. Copy-paste each block into a separate Tally form.

Repo (use for all 3): **https://github.com/ritwikareddykancharla/peec-mcp-challenge**
Peec project: **https://app.peec.ai/projects/or_45c84dd8-183b-42ae-9598-1956575af925**

---

## Submission 1 — Citation Gap Brief Generator

**Workflow name:** Citation Gap Brief Generator
**Suggested category:** Content Optimization
**Tools used:** Claude Desktop + Peec MCP
**Repo:** https://github.com/ritwikareddykancharla/peec-mcp-challenge/tree/main/workflow-1-content-optimization

### Description

Marketing teams know they have AI-search blind spots. Peec tells them which prompts and competitors are stealing their visibility. This workflow closes the loop — it tells them exactly what to write next.

A Claude Desktop project loaded with a custom system prompt and the Peec MCP server. Three slash commands:

- `/find-gaps` — pulls `get_domain_report` with the gap filter to surface domains where competitors get cited but Linear doesn't.
- `/brief <rank>` — for any gap, calls `get_url_report` + `get_url_content` to scrape the top cited competitor URLs, then auto-generates a full content brief: target prompt, engines affected, competing-content analysis, recommended H1/H2 outline, internal-link plan, distribution recommendation.
- `/weekly-gap-report` — Monday-morning ritual: combines gap data with `get_actions(scope=editorial)` for a one-page report ready to paste into Notion.

Replaces ~3 hours of manual brief-building per week. Built to run weekly, forever. Shared with #BuiltWithPeec.

---

## Submission 2 — AI Engine Movement Alerts

**Workflow name:** AI Engine Movement Alerts
**Suggested category:** Competitive Analysis
**Tools used:** Claude Desktop + Peec MCP
**Repo:** https://github.com/ritwikareddykancharla/peec-mcp-challenge/tree/main/workflow-2-competitive-analysis

### Description

Most AI-visibility dashboards give you one number. The story isn't the number — it's the **delta** and the **engine**. Linear can be #2 on Claude and #8 on Gemini, and that's the whole insight.

A Claude Desktop project that detects week-over-week shifts in AI-engine visibility, broken down per engine (ChatGPT, Gemini, Claude, AI Mode, Perplexity), and surfaces them as Slack-ready alerts.

- `/snapshot` — per-engine matrix of visibility for Linear vs 6 competitors.
- `/digest` — pulls two `get_brand_report` windows (current 7d vs prior 7d), computes deltas per (brand × engine), flags critical movements with severity emojis, and pulls actual chat snippets via `list_chats` + `get_chat` to show *why* something changed.
- `/investigate <prompt>` — answers "are we in the conversation for X?" with per-engine evidence from real AI responses.

Designed for daily Slack drops or weekly standups. Tunable thresholds. #BuiltWithPeec.

---

## Submission 3 — Monthly Executive AI-Visibility Brief

**Workflow name:** Monthly Executive AI-Visibility Brief
**Suggested category:** Reporting Automation
**Tools used:** Claude Desktop + Peec MCP
**Repo:** https://github.com/ritwikareddykancharla/peec-mcp-challenge/tree/main/workflow-3-reporting-automation

### Description

Building the monthly leadership AI-visibility report manually means: pulling reports, computing month-over-month deltas, ranking prompts, cross-referencing citation gaps, prioritizing actions, then writing prose. Every. Single. Month.

This workflow does it in one prompt. A Claude Desktop project enforces a strict, board-ready output structure that combines:

- Current vs prior 30-day brand metrics (`get_brand_report` ×2)
- Per-engine performance breakdown (`get_brand_report` dim=model_id)
- Top 5 winning prompts + top 5 losing prompts (`get_brand_report` dim=prompt_id)
- Top 5 citation sources marked ✅/❌ for Linear coverage (`get_domain_report`)
- 3 prioritized actions sourced from `get_actions(scope=overview)`
- One strategic question for the leadership team

Three slash commands: `/exec-brief` (full report), `/section <n>` (regenerate one section), `/email-version` (200-word email reformat). Same data, three audiences.

Replaces ~4 hours of analyst work per month. Output is identical month-over-month, so reports are directly comparable. #BuiltWithPeec.

---

## Suggested public posts (for #BuiltWithPeec)

A 3-tweet thread (or 3 standalone LinkedIn posts), one per workflow.

### Tweet 1 — Content Optimization

> Built 3 workflows for the @peec_ai MCP Challenge — one per category. 🧵
>
> 1/ Citation Gap Brief Generator
> Finds the AI-cited URLs where competitors get cited but my brand doesn't, scrapes them via the Peec MCP, and outputs a ready-to-write content brief. Replaces hours of manual SERP research per week.
>
> Repo: github.com/ritwikareddykancharla/peec-mcp-challenge
> #BuiltWithPeec

### Tweet 2 — Competitive Analysis

> 2/ AI Engine Movement Alerts
>
> Most AI-visibility tools give you one number. The story isn't the number — it's the delta and the engine.
>
> This Claude Desktop workflow snapshots every brand × engine combo, computes week-over-week deltas, and surfaces critical movements as Slack-ready alerts — with actual chat snippets pulled via the Peec MCP showing *why* something shifted.
>
> Per-engine breakdown is the unlock. You can be #2 on Claude and #8 on Gemini, and that's the whole insight.
>
> Repo: github.com/ritwikareddykancharla/peec-mcp-challenge
> #BuiltWithPeec

### Tweet 3 — Reporting Automation

> 3/ Monthly Executive AI-Visibility Brief
>
> Building the monthly leadership report manually = pull data, compute MoM deltas, rank prompts, cross-reference citations, write prose. Every. Month.
>
> One slash command in Claude Desktop now does it all via the Peec MCP — board-ready output in ~30 seconds. Same structure every month, so reports are directly comparable.
>
> Three formats from one prompt: long markdown for Notion, sectioned for revision, prose for email.
>
> Repo: github.com/ritwikareddykancharla/peec-mcp-challenge
> #BuiltWithPeec

### Wrap-up tweet (optional)

> All three workflows in one repo. Built in Claude Desktop with the Peec MCP. Designed to actually run on a real cadence — weekly, daily, monthly — not just demo once.
>
> If you're tracking AI search visibility, this is the toolkit. 👇
> github.com/ritwikareddykancharla/peec-mcp-challenge
> #BuiltWithPeec @peec_ai
