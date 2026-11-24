# Capital Signal MCP Server

Remote [Model Context Protocol (MCP)](https://modelcontextprotocol.io) server for **[Capital Signal](https://capitalsignal.io)** — every ASX announcement since 2018 extracted into structured, filing-linked data.

- **Website (daily ASX front page):** https://capitalsignal.io
- **Company dossiers (all ASX tickers):** https://capitalsignal.io/c
- **Research & desk notes:** https://capitalsignal.io/research
- **Setup guide (Claude, ChatGPT, Cursor, Codex):** https://capitalsignal.io/connect
- **Remote MCP endpoint:** `https://capitalsignal.io/api/mcp`

## What it does

Ask Claude, ChatGPT, Cursor, or any MCP client plain-English questions about ASX-listed companies and get structured numbers linked directly to the primary ASX PDF filing:

- **Capital raises:** placements, SPPs, entitlement offers, discounts, lead managers, tranche splits, and post-raise performance.
- **Substantial holders:** entries, exits, stake changes, and cross-company holder clusters (excluding stock lending by default).
- **Director trading:** genuine on- and off-market buys and sales in A$ (separating out option exercises, vestings, and tax-on-vesting sales).
- **M&A & schemes:** binding schemes, takeover bids, non-binding proposals, premiums, and conditions.
- **Cash & runway:** Appendix 4C/5B quarterly cash balances, burn rates, and runway adjusted for subsequent raises.
- **Guidance & updates:** upgrades, downgrades, trading updates, buybacks, and distress notices.
- **Mining projects & drill intercepts:** named projects, stages, commodities, and gram-metre ranked intercepts.
- **Board track records:** director history across ASX boards (takeovers, dilution, excess returns).
- **Full-text filing search & reader:** search across all ASX filings and read full extracted text section by section.

## Quick connect

1. Visit **https://capitalsignal.io/connect** to connect via OAuth or create a free API key.
2. Add the remote MCP server URL to your client:

```json
{
  "mcpServers": {
    "capital-signal": {
      "url": "https://capitalsignal.io/api/mcp"
    }
  }
}
```

Full documentation and tool reference: **https://capitalsignal.io/docs**

## Example prompts

- *"Which ASX lithium or copper explorers have under 2 quarters of cash left and have not raised since quarter end?"*
- *"Show every ASX capital raise over A$10m in the last 90 days, ranked by discount to last close."*
- *"Who are the substantial holders in BET and when did they enter?"*
- *"Which ASX companies upgraded earnings guidance this month?"*

## License

MIT — this repository hosts public documentation and registry metadata for the hosted Capital Signal MCP server.
