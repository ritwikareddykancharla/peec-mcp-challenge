# Demo Script — Workflow 3

A 3-minute walkthrough you can record for your hackathon submission.

## Setup shot
- Claude Desktop with "Linear — Monthly Exec Brief" project loaded.
- Peec MCP server connected.

## Step 1 — Generate the full brief (90s)

```
/exec-brief
```

**Expected output:** Full one-page report with: headline, this-month vs prior-month metrics table, per-engine performance, top 5 winning prompts, top 5 losing prompts, top citation sources (✅/❌), 3 prioritized actions, one strategic question.

**Talking point:** "What you're seeing took one prompt and ~30 seconds. Manually this is half a day of analyst work — pulling reports, computing deltas, ranking prompts, cross-referencing citations, writing prose. Every month."

## Step 2 — Iterate on a section (45s)

```
/section 4
```

**Expected output:** Just Section 4 (Losing Prompts) regenerated, perhaps with deeper analysis or a different sort.

**Talking point:** "Mid-cycle, if a section feels thin or data updated, regenerate just that section. Same structure, new data, no need to re-run the whole report."

## Step 3 — Reformat for distribution (45s)

```
/email-version
```

**Expected output:** A 200-word email-ready version with subject line — plain prose, no tables.

**Talking point:** "Same brief, three formats: long markdown for Notion, sectioned for revision, prose for email. One prompt's data, repurposed for every audience."

## Closing
- Project link: https://app.peec.ai/projects/or_45c84dd8-183b-42ae-9598-1956575af925
- #BuiltWithPeec
- "Three workflows, three categories, all powered by Peec MCP, all running monthly with zero manual lift."
