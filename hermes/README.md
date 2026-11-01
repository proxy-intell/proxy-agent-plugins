# Proxy for Hermes Agent

Creative strategy and marketing engineering on live ad data. Find the hooks, angles and offers working for competitors, brief new creatives from them, and put competitor tracking on a schedule. Proxy connects Hermes to the hosted Proxy MCP server at `mcp.useproxy.dev`.

- **Meta:** a brand's live Facebook and Instagram ads, or keyword search across the Meta Ad Library.
- **Google:** ads from the Google Ads Transparency Center, with creative variations and targeting.
- **LinkedIn and TikTok:** LinkedIn Ad Library and TikTok's EU ad library.
- **Analysis:** video ad transcripts, image breakdowns, competitor discovery, cross-platform briefs.

Read-only. Proxy never touches your ad accounts.

## Install

```
hermes plugins install proxy
hermes plugins enable proxy
```

Requires Node.js 20.18.1+ and npm. Sign-in runs through `npx mcp-remote@0.1.49` (pinned) because Hermes does not run OAuth for MCP servers declared by a plugin.

Prefer no Node? Skip the plugin and add the server directly to `~/.hermes/config.yaml`:

```yaml
mcp_servers:
  proxy:
    url: "https://mcp.useproxy.dev/mcp?ref=hermes"
    auth: oauth
```

Then run `hermes mcp login proxy`.

## Sign in

On first use a browser window opens. Sign in with Google. No API keys.

## Example prompts

- "What ads is Notion running on Meta and Google right now?"
- "Who are my competitors, and what are their best TikTok ads?"
- "Transcribe the longest-running video ad from Gymshark."
- "Brief 5 ad concepts from our competitors' longest-running hooks."
- "Every Monday, show me new ads from these five brands." (Hermes cron)

## Pricing

Free: 20 credits a day, no card. Most calls cost 1 credit. Paid plans: https://useproxy.dev/pricing

## Disclosures

- **Network:** every tool call goes to `mcp.useproxy.dev`. Your queries (brand names, keywords, ad URLs) are sent there.
- **Sign-in:** runs `npx mcp-remote@0.1.49` from the npm registry. It stores OAuth tokens in `~/.mcp-auth`.
- **Unattended runs:** the first sign-in needs a browser, so sign in in an interactive chat before scheduling cron jobs.
- **Writes:** none. Every tool reads public ad libraries.
- **Telemetry:** Proxy logs tool usage server-side for billing and product analytics. The plugin itself sends nothing.

Privacy policy: https://useproxy.dev/privacy
