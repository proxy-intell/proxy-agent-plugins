---
name: ad-swipe-file
description: "A swipe file of ad references, grouped by visual pattern. Use when the user wants ad inspiration and swipe files: static ad references, design ideas, visual patterns, plus organic TikTok and Instagram references. Runs on Proxy, the live Meta, Google, LinkedIn and TikTok ad library MCP."
---

# A swipe file of ad references, grouped by visual pattern

Runs on [Proxy](https://useproxy.dev/playbooks/ad-swipe-file?utm_source=mcp&utm_medium=skill): live Meta, Google, LinkedIn and TikTok (EU) ad libraries over MCP. OAuth, no API keys, free for 20 credits a day.

## Setup

If Proxy's tools (`get_playbook`, `get_meta_ads`) are not available, Proxy is not connected. Tell the user how, then stop:

- Claude Code: `claude mcp add --transport http proxy 'https://mcp.useproxy.dev/mcp?ref=skill-ad-swipe-file'`, then `/mcp` to sign in
- Claude, ChatGPT, Cursor and other clients: https://useproxy.dev/welcome?utm_source=mcp&utm_medium=skill

## Run

1. Call `get_playbook` with job `creative_refs` (free). It returns the current method: exact tool calls, what to look for, and the output format.
2. Follow it step by step. Inputs it needs: what the references are for (product, medium: static, video, carousel), named brands or a category, market.
3. Deliver its output, ready to use, and end with its coverage line.
