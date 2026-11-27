# Claude Code

Set `KLAREFI_API_KEY` in the environment Claude Code starts from, then run:

```sh
claude plugin marketplace add jmqcooper-ai/klarefi-mcp
claude plugin install klarefi@klarefi
claude mcp list
```

Open a new session and run `/mcp` to see the tools. To remove it, run
`claude plugin uninstall klarefi@klarefi`.

Set the key before you start Claude Code. Without it, Claude Code sends the
placeholder `${KLAREFI_API_KEY}` as the key and customer tools fail.

To add only the MCP server, without the plugin, follow the
[manual setup](https://www.klarefi.com/docs/api/connect-assistants#claude-code).
