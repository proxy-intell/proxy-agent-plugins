---
name: who-is-advertising
description: "Which businesses on a list run ads, and an opener for each. Use when the user wants which businesses, locations or prospects run ads; prospect lists, newly launched brands. Runs on Proxy, the live Meta, Google, LinkedIn and TikTok ad library MCP."
---

# Which businesses on a list run ads, and an opener for each

Runs on [Proxy](https://useproxy.dev/playbooks/who-is-advertising?utm_source=mcp&utm_medium=skill): live Meta, Google, LinkedIn and TikTok (EU) ad libraries over MCP. OAuth, no API keys, free for 20 credits a day.

## Setup

If Proxy's tools (`get_playbook`, `get_meta_ads`) are not available, Proxy is not connected. Tell the user how, then stop:

- Claude Code: `claude mcp add --transport http proxy 'https://mcp.useproxy.dev/mcp?ref=skill-who-is-advertising'`, then `/mcp` to sign in
- Claude, ChatGPT, Cursor and other clients: https://useproxy.dev/welcome?utm_source=mcp&utm_medium=skill

## Run

1. Call `get_playbook` with job `who_is_advertising` (free). It returns the current method: exact tool calls, what to look for, and the output format.
2. Follow it step by step. Inputs it needs: names or domains. Only a market given: build the list with search_competitors(description="<market and city or country>") or local advertisers from search_meta_ads_by_keyword(query="<service>", country="<XX>"). Newly launched brands: search_meta_ads_by_keyword(query="<category>", country="<XX>", sort_by="newest", limit=60), group by page_id, then get_meta_ads(platform_ids=["<page_id>", "<page_id>"], status="all", limit=50) and keep pages whose oldest ad of any status started inside the window asked and that meet any minimum ad count. A page that hit the limit may be older: not new.
3. Deliver its output, ready to use, and end with its coverage line.
