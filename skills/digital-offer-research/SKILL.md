---
name: digital-offer-research
description: "Digital products and info offers that keep paying for ads, and how they sell. Use when the user wants digital products and info offers: courses, ebooks, coaching, templates, low-ticket funnels, VSLs. Runs on Proxy, the live Meta, Google, LinkedIn and TikTok ad library MCP."
---

# Digital products and info offers that keep paying for ads, and how they sell

Runs on [Proxy](https://useproxy.dev/playbooks/digital-offer-research?utm_source=mcp&utm_medium=skill): live Meta, Google, LinkedIn and TikTok (EU) ad libraries over MCP. OAuth, no API keys, free for 20 credits a day.

## Setup

If Proxy's tools (`get_playbook`, `get_meta_ads`) are not available, Proxy is not connected. Tell the user how, then stop:

- Claude Code: `claude mcp add --transport http proxy 'https://mcp.useproxy.dev/mcp?ref=skill-digital-offer-research'`, then `/mcp` to sign in
- Claude, ChatGPT, Cursor and other clients: https://useproxy.dev/welcome?utm_source=mcp&utm_medium=skill

## Run

1. Call `get_playbook` with job `digital_offer` (free). It returns the current method: exact tool calls, what to look for, and the output format.
2. Follow it step by step. Inputs it needs: market (country, language), niche or problem, price tier if known (low-ticket, mid, high-ticket).
3. Deliver its output, ready to use, and end with its coverage line.
