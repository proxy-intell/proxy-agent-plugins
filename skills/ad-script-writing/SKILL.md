---
name: ad-script-writing
description: "Original ad scripts built on structures that have run for months. Use when the user wants video ad scripts, hooks to film, UGC briefs, static or advertorial copy, modelling or recreating a winning ad, trending organic TikTok and Instagram hooks to bring into paid. Runs on Proxy, the live Meta, Google, LinkedIn and TikTok ad library MCP."
---

# Original ad scripts built on structures that have run for months

Runs on [Proxy](https://useproxy.dev/playbooks/ad-script-writing?utm_source=mcp&utm_medium=skill): live Meta, Google, LinkedIn and TikTok (EU) ad libraries over MCP. OAuth, no API keys, free for 20 credits a day.

## Setup

If Proxy's tools (`get_playbook`, `get_meta_ads`) are not available, Proxy is not connected. Tell the user how, then stop:

- Claude Code: `claude mcp add --transport http proxy 'https://mcp.useproxy.dev/mcp?ref=skill-ad-script-writing'`, then `/mcp` to sign in
- Claude, ChatGPT, Cursor and other clients: https://useproxy.dev/welcome?utm_source=mcp&utm_medium=skill

## Run

1. Call `get_playbook` with job `script_writing` (free). It returns the current method: exact tool calls, what to look for, and the output format.
2. Follow it step by step. Inputs it needs: product, audience, offer. Infer missing ones from the conversation or their site and state them.
3. Deliver its output, ready to use, and end with its coverage line.
