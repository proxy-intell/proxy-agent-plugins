---
name: brand-ad-audit
description: "One brand's ads audited against category leaders, for a pitch or sales call. Use when the user wants auditing one brand's ads against category leaders; agency pitch or sales call prep. Runs on Proxy, the live Meta, Google, LinkedIn and TikTok ad library MCP."
---

# One brand's ads audited against category leaders, for a pitch or sales call

Runs on [Proxy](https://useproxy.dev/playbooks/brand-ad-audit?utm_source=mcp&utm_medium=skill): live Meta, Google, LinkedIn and TikTok (EU) ad libraries over MCP. OAuth, no API keys, free for 20 credits a day.

## Setup

If Proxy's tools (`get_playbook`, `get_meta_ads`) are not available, Proxy is not connected. Tell the user how, then stop:

- Claude Code: `claude mcp add --transport http proxy 'https://mcp.useproxy.dev/mcp?ref=skill-brand-ad-audit'`, then `/mcp` to sign in
- Claude, ChatGPT, Cursor and other clients: https://useproxy.dev/welcome?utm_source=mcp&utm_medium=skill

## Run

1. Call `get_playbook` with job `ad_audit` (free). It returns the current method: exact tool calls, what to look for, and the output format.
2. Follow it step by step. Inputs it needs: the brand (name or domain), its market, 2-3 leaders to benchmark (else find them).
3. Deliver its output, ready to use, and end with its coverage line.
