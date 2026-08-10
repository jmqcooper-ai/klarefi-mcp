# Klarefi MCP

Klarefi completes regulated intake work before a person reviews the case. The
MCP server can guide applicants, read cited case files, manage workflow drafts,
and run approved connector actions. It does not decide a case.

## Hosted server

Use the hosted Streamable HTTP endpoint:

```text
https://www.klarefi.com/mcp
```

[Choose an MCP client and connect Klarefi](https://install.apicommons.org/?server=https%3A%2F%2Fwww.klarefi.com%2F.well-known%2Fmcp%2Fserver.json)

Customer tools require this header:

```text
Authorization: Bearer KLAREFI_API_KEY
```

Applicant tools can use a signed intake URL without an API key.

## Client packages

This repository includes ready-to-publish metadata for Codex, Claude, Cursor,
and Antigravity. Each package connects to the same hosted server.

- Codex: `.codex-plugin/plugin.json` and `.mcp.json`
- Claude: `.claude-plugin/plugin.json` and `mcp.json`
- Cursor: `.cursor-plugin/plugin.json` and `mcp.json`
- Antigravity: `plugin.json` and `mcp_config.json`
- MCP Registry: `server.json`

For a local stdio client, run `bunx --bun @klarefi/mcp`.

## Links

- [Documentation](https://www.klarefi.com/docs/guides/agent-intake)
- [Privacy](https://www.klarefi.com/privacy)
- [Terms](https://www.klarefi.com/terms)
- [Support](mailto:support@klarefi.com)
