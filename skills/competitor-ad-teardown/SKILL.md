---
name: competitor-ad-teardown
description: "How competitors sell: angles, hooks, offers, formats, gaps. Use when the user wants competitors' hooks, offers, angles and positioning, what's working in a market, local service competitors. Runs on Proxy, the live Meta, Google, LinkedIn and TikTok ad library MCP."
---

# How competitors sell: angles, hooks, offers, formats, gaps

Runs on [Proxy](https://useproxy.dev/playbooks/competitor-ad-teardown?utm_source=mcp&utm_medium=skill): live Meta, Google, LinkedIn and TikTok (EU) ad libraries over MCP. OAuth, no API keys, free for 20 credits a day.

## Setup

If Proxy's tools (`get_playbook`, `get_meta_ads`) are not available, Proxy is not connected. Tell the user how, then stop:

- Claude Code: `claude mcp add --transport http proxy 'https://mcp.useproxy.dev/mcp?ref=skill-competitor-ad-teardown'`, then `/mcp` to sign in
- Claude, ChatGPT, Cursor and other clients: https://useproxy.dev/welcome?utm_source=mcp&utm_medium=skill

## Run

1. Call `get_playbook` with job `competitor_teardown` (free). It returns the current method: exact tool calls, what to look for, and the output format.
2. Follow it step by step. Inputs it needs: competitors or market, the user's own brand if any, country if named.
3. Deliver its output, ready to use, and end with its coverage line.
