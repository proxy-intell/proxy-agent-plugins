---
name: competitor-ad-watch
description: "What competitors launched, dropped and kept since last time. Use when the user wants tracking or monitoring competitors, what's new, weekly or daily updates. Runs on Proxy, the live Meta, Google, LinkedIn and TikTok ad library MCP."
---

# What competitors launched, dropped and kept since last time

Runs on [Proxy](https://useproxy.dev/playbooks/competitor-ad-watch?utm_source=mcp&utm_medium=skill): live Meta, Google, LinkedIn and TikTok (EU) ad libraries over MCP. OAuth, no API keys, free for 20 credits a day.

## Setup

If Proxy's tools (`get_playbook`, `get_meta_ads`) are not available, Proxy is not connected. Tell the user how, then stop:

- Claude Code: `claude mcp add --transport http proxy 'https://mcp.useproxy.dev/mcp?ref=skill-competitor-ad-watch'`, then `/mcp` to sign in
- Claude, ChatGPT, Cursor and other clients: https://useproxy.dev/welcome?utm_source=mcp&utm_medium=skill

## Run

1. Call `get_playbook` with job `competitor_watch` (free). It returns the current method: exact tool calls, what to look for, and the output format.
2. Follow it step by step.
3. Deliver its output, ready to use, and end with its coverage line.
