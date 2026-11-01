# Proxy agent plugins

[Proxy](https://useproxy.dev) gives AI agents live ads from the Meta Ad Library, Google Ads Transparency Center, LinkedIn Ad Library and TikTok's EU ad library. Use it for creative strategy, marketing engineering and competitor research. Read-only, no API keys, free tier of 20 credits a day.

| Path | For |
| --- | --- |
| [`hermes/`](hermes) | Hermes Agent plugin (skill + MCP server) |
| [`skills/proxy-ad-research/`](skills/proxy-ad-research) | The skill alone, for Hermes taps, OpenClaw/ClawHub and any Agent Skills client |

## Hermes

Skill only, available now:

```
hermes skills tap add proxy-intell/proxy-agent-plugins
```

Full plugin (skill + sign-in), once it is in the Hermes plugin catalog:

```
hermes plugins install proxy
hermes plugins enable proxy
```

Or add `mcp_servers.proxy` yourself, see [`hermes/README.md`](hermes/README.md).

## OpenClaw

```
openclaw mcp set proxy '{"url":"https://mcp.useproxy.dev/mcp?ref=openclaw","transport":"streamable-http","auth":"oauth"}'
openclaw mcp login proxy
```

Skill: search `proxy-ad-research` on ClawHub.

## Any MCP client

Connect to `https://mcp.useproxy.dev/mcp`. Setup for every client: https://useproxy.dev/welcome

The canonical skill lives at https://useproxy.dev/SKILL.md. MIT licensed.
