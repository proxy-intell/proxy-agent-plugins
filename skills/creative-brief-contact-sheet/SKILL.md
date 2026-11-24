---
name: creative-brief-contact-sheet
description: "A creative brief with a contact sheet: the reference ads behind it on one labelled grid. Use when the user wants creative, design, shoot or video briefs, mood boards, contact sheets of reference ads for a designer, editor, creator or agency. Runs on Proxy, the live Meta, Google, LinkedIn and TikTok ad library MCP."
---

# A creative brief with a contact sheet: the reference ads behind it on one labelled grid

Runs on [Proxy](https://useproxy.dev/playbooks/creative-brief-contact-sheet?utm_source=mcp&utm_medium=skill): live Meta, Google, LinkedIn and TikTok (EU) ad libraries over MCP. OAuth, no API keys, free for 20 credits a day.

## Setup

If Proxy's tools (`get_playbook`, `get_meta_ads`) are not available, Proxy is not connected. Tell the user how, then stop:

- Claude Code: `claude mcp add --transport http proxy 'https://mcp.useproxy.dev/mcp?ref=skill-creative-brief-contact-sheet'`, then `/mcp` to sign in
- Claude, ChatGPT, Cursor and other clients: https://useproxy.dev/welcome?utm_source=mcp&utm_medium=skill

## Run

1. Call `get_playbook` with job `contact_sheet` (free). It returns the current method: exact tool calls, what to look for, and the output format.
2. Follow it step by step. Inputs it needs: product, what the brief is for (static, video, UGC, carousel), audience, offer, named brands or a category, market. Infer missing ones from the conversation or their site and state them.
3. Deliver its output, ready to use, and end with its coverage line.
