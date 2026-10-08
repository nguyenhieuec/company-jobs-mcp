# Install Company Jobs Finder (for AI agents)

This is a hosted remote MCP server. There is nothing to clone, build or run locally.

1. Add a remote MCP server named `openkrill-company-jobs` with transport Streamable HTTP and URL `https://jobs.openkrill.app/mcp`.
   No API key, header or environment variable is needed.
2. Cline: run `cline mcp install openkrill-company-jobs --transport http https://jobs.openkrill.app/mcp`, or add this to `cline_mcp_settings.json`:

```json
{
  "mcpServers": {
    "openkrill-company-jobs": {
      "type": "streamableHttp",
      "url": "https://jobs.openkrill.app/mcp",
      "disabled": false
    }
  }
}
```

3. Check the install by listing the server's tools. You should see the tools in the README.md table, for example `find_company_jobs`.
