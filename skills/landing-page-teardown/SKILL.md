---
name: landing-page-teardown
description: "The pages long-running ads send traffic to, and how they're built. Use when the user wants landing pages, sales pages and funnels behind long-running ads. Runs on Proxy, the live Meta, Google, LinkedIn and TikTok ad library MCP."
---

# The pages long-running ads send traffic to, and how they're built

Runs on [Proxy](https://useproxy.dev/playbooks/landing-page-teardown?utm_source=mcp&utm_medium=skill): live Meta, Google, LinkedIn and TikTok (EU) ad libraries over MCP. OAuth, no API keys, free for 20 credits a day.

## Setup

If Proxy's tools (`get_playbook`, `get_meta_ads`) are not available, Proxy is not connected. Tell the user how, then stop:

- Claude Code: `claude mcp add --transport http proxy 'https://mcp.useproxy.dev/mcp?ref=skill-landing-page-teardown'`, then `/mcp` to sign in
- Claude, ChatGPT, Cursor and other clients: https://useproxy.dev/welcome?utm_source=mcp&utm_medium=skill

## Run

1. Call `get_playbook` with job `landing_teardown` (free). It returns the current method: exact tool calls, what to look for, and the output format.
2. Follow it step by step. Inputs it needs: brands or a category, market.
3. Deliver its output, ready to use, and end with its coverage line.
