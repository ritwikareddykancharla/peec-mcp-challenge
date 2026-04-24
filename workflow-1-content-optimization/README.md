# Workflow 1 — Citation Gap Brief Generator

**Category:** Content Optimization
**Stack:** Claude Desktop + Peec AI MCP server
**Built with:** #BuiltWithPeec

## What it does

Turns Peec's citation-gap data into ready-to-write SEO content briefs. Every week (or on demand), it finds the URLs that AI engines cite about project management — but where Linear is missing — then scrapes those competitor pages and outputs a structured brief a content writer can pick up immediately.

## Why it matters

Marketing teams already know they have AI-search blind spots. Peec tells you *which* prompts and which competitors are stealing your visibility. This workflow closes the loop: it tells you **exactly what to write next** and why, with competitive analysis baked in.

Replaces ~3 hours per brief of manual SERP research, scraping, and gap analysis.

## Setup (3 minutes)

1. **Install Claude Desktop** if you don't already have it: https://claude.ai/download
2. **Install the Peec MCP server** in Claude Desktop. In Claude Desktop settings → Connectors → Add MCP server and follow the Peec setup at https://docs.peec.ai/mcp.
3. **Create a Claude Desktop Project** called "Linear — Citation Gap Briefs".
4. **Paste the contents of `system-prompt.md`** into the project's *Custom instructions*.
5. Open the project and try the demo script below.

## Demo

Open the Claude Desktop project and type:

```
/find-gaps
```

Then:

```
/brief 1
```

Then once a week:

```
/weekly-gap-report
```

See `demo-script.md` for the full guided walkthrough.

## How it uses Peec MCP

| Step | Peec tool | Purpose |
|---|---|---|
| Find gap domains | `get_domain_report` (gap=true) | Domains citing competitors but not Linear |
| Find gap URLs | `get_url_report` (gap=true) | Specific competitor-cited pages |
| Read competitor content | `get_url_content` | Scraped markdown of cited pages |
| Weekly recommendations | `get_actions` (scope=editorial) | Editorial action backlog |
| Engine breakdown | `get_brand_report` (dim=model_id) | Per-engine performance |

## Repeatability

Designed to run **weekly** as a recurring workflow. Each `/weekly-gap-report` produces a fresh brief that the content team can ship. The system prompt enforces strict, repeatable output structure so reports are comparable week over week.

## Project link

https://app.peec.ai/projects/or_45c84dd8-183b-42ae-9598-1956575af925
