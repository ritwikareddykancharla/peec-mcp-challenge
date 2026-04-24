# Demo Script — Workflow 2

A 3-minute walkthrough you can record for your hackathon submission.

## Setup shot
- Claude Desktop with "Linear — Competitive Movement Alerts" project loaded.
- Peec MCP server connected.

## Step 1 — Snapshot the current state (45s)

```
/snapshot
```

**Expected output:** Per-engine matrix showing Linear vs 6 competitors, with ⚠️ markers on weak engines.

**Talking point:** "Most tools give you one number. Peec lets us slice by engine — and that's where the story lives. Here, Linear is strong on Claude but invisible on Gemini."

## Step 2 — See what changed (75s)

```
/digest
```

**Expected output:** Slack-ready digest with 🚨 Critical, ⚠️ Watch, ✅ Wins sections, plus quoted chat snippets showing why Linear lost ground.

**Talking point:** "This is the alert I wish I had. It's not 'here are the numbers' — it's 'here's what changed this week, on which engine, and here's the actual sentence from ChatGPT that's hurting us.' I can drop this straight into Slack."

## Step 3 — Drill into a specific prompt (45s)

```
/investigate best project management tool for engineering teams
```

**Expected output:** Per-engine table showing how each AI currently answers that prompt — which brands appear, in what order, with what framing.

**Talking point:** "When the CMO asks 'are we in the conversation for X?' — this is the answer. Five engines, real chat data, Peec's chat tool surfacing the actual responses."

## Step 4 — Show the rules (15s)

```
/alert-rules
```

**Talking point:** "Tunable thresholds. Run daily as a Slack workflow, weekly as a standup brief, or on-demand."

## Closing
- Project link: https://app.peec.ai/projects/or_45c84dd8-183b-42ae-9598-1956575af925
- #BuiltWithPeec
