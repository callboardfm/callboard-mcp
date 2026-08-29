# Callboard MCP Connector

[Callboard](https://www.callboard.fm) is booking intelligence for independent concert
promoters. This connector lets an AI assistant run and read **Promoter Briefs** —
market fit score, venue sizing, tiered pricing, deal economics and risk flags for an
"should I book this artist in this market?" question — under your Callboard account.

> This repository holds the connector's public metadata (`server.json`) for MCP
> registries. The server itself is a hosted service; there is nothing to install.

## Connect

| Client | URL |
|---|---|
| Claude (claude.ai, Desktop, mobile) | `https://api.callboard.fm/mcp` |
| Claude Code | `claude mcp add --transport http callboard https://api.callboard.fm/mcp` |
| ChatGPT (Plus and up, developer mode) | `https://api.callboard.fm/sse/` |

Sign in with your Callboard account when prompted — OAuth 2.1, no API keys.
Full setup guide: **https://www.callboard.fm/docs/mcp**

## What it can do

| Tool | |
|---|---|
| `run_brief` | Start a Promoter Brief for an artist + market question (~5 minutes; uses one brief from your monthly allowance) |
| `get_brief_job` | Progress of a running brief; the memo and full brief when it finishes |
| `get_brief` / `list_briefs` | Read and browse your (and your team's) brief history |
| `search_artists` | Resolve which artist you mean |
| `get_watchlist` | Artists you're watching |
| `get_account` | Plan and remaining allowance |
| `search` / `fetch` | ChatGPT connector contract over your briefs |

Reading tools are read-only annotated; `run_brief` is the only tool that spends
anything. The connector is included on the **Buyer** and **Company** plans —
see [pricing](https://www.callboard.fm/pricing).

## Privacy & support

- Privacy policy: https://www.callboard.fm/privacy
- Support: support@callboard.fm
