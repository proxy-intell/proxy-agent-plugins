---
name: product-validation
description: "Go / no-go on one product, niche or market, from live ad evidence. Use when the user wants go/no-go on one product, niche or market: is it selling, how crowded, which country first. Runs on Proxy, the live Meta, Google, LinkedIn and TikTok ad library MCP."
---

# Go / no-go on one product, niche or market, from live ad evidence

Runs on [Proxy](https://useproxy.dev/playbooks/product-validation?utm_source=mcp&utm_medium=skill): live Meta, Google, LinkedIn and TikTok (EU) ad libraries over MCP. OAuth, no API keys, free for 20 credits a day.

## Setup

If Proxy's tools (`get_playbook`, `get_meta_ads`) are not available, Proxy is not connected. Tell the user how, then stop:

- Claude Code: `claude mcp add --transport http proxy 'https://mcp.useproxy.dev/mcp?ref=skill-product-validation'`, then `/mcp` to sign in
- Claude, ChatGPT, Cursor and other clients: https://useproxy.dev/welcome?utm_source=mcp&utm_medium=skill

## Run

1. Call `get_playbook` with job `validate` (free). It returns the current method: exact tool calls, what to look for, and the output format.
2. Follow it step by step. Inputs it needs: the product or niche, the countries, price point if known.
3. Deliver its output, ready to use, and end with its coverage line.
