---
name: holiday-ad-campaigns
description: "What brands ran for a season, week by week, and what to run. Use when the user wants seasonal campaigns (Black Friday, Christmas, 11.11, Ramadan, Valentine's): what ran when, what to run. Runs on Proxy, the live Meta, Google, LinkedIn and TikTok ad library MCP."
---

# What brands ran for a season, week by week, and what to run

Runs on [Proxy](https://useproxy.dev/playbooks/holiday-ad-campaigns?utm_source=mcp&utm_medium=skill): live Meta, Google, LinkedIn and TikTok (EU) ad libraries over MCP. OAuth, no API keys, free for 20 credits a day.

## Setup

If Proxy's tools (`get_playbook`, `get_meta_ads`) are not available, Proxy is not connected. Tell the user how, then stop:

- Claude Code: `claude mcp add --transport http proxy 'https://mcp.useproxy.dev/mcp?ref=skill-holiday-ad-campaigns'`, then `/mcp` to sign in
- Claude, ChatGPT, Cursor and other clients: https://useproxy.dev/welcome?utm_source=mcp&utm_medium=skill

## Run

1. Call `get_playbook` with job `holiday_teardown` (free). It returns the current method: exact tool calls, what to look for, and the output format.
2. Follow it step by step. Inputs it needs: brands or a category, the season, the market. Window: 6 weeks before the day to 1 week after.
3. Deliver its output, ready to use, and end with its coverage line.
