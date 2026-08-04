# mcp-data-angers

Angers Loire Métropole Open Data (data.angers.fr) — OpenDataSoft MCP.

Part of [Pipeworx](https://pipeworx.io) — an MCP gateway connecting AI agents to 1394+ live data sources.

## Tools

| Tool | Description |
|------|-------------|
| `search_datasets` | Search Angers Loire Métropole Open Data for datasets by keyword (mobility, urban services & environment). Returns dataset_ids (pass to query/dataset_info), titles, themes and record counts. |
| `dataset_info` | Get metadata for one Angers Loire Métropole Open Data dataset (fields/schema, themes, record count) — call before query to learn the column names. |
| `query` | Query records from a Angers Loire Métropole Open Data dataset with ODSQL. Filter (where), aggregate (group_by/select), sort (order_by), paginate (limit/offset). |

## Quick Start

Add to your MCP client (Claude Desktop, Cursor, Windsurf, etc.):

```json
{
  "mcpServers": {
    "data-angers": {
      "url": "https://gateway.pipeworx.io/data-angers/mcp"
    }
  }
}
```

Or connect to the full Pipeworx gateway for access to all 1394+ data sources:

```json
{
  "mcpServers": {
    "pipeworx": {
      "url": "https://gateway.pipeworx.io/mcp"
    }
  }
}
```

## Using with ask_pipeworx

Instead of calling tools directly, you can ask questions in plain English:

```
ask_pipeworx({ question: "your question about Data Angers data" })
```

The gateway picks the right tool and fills the arguments automatically.

## More

- [Docs and guides](https://pipeworx.io/docs)
- [pipeworx.io](https://pipeworx.io)

## License

MIT
