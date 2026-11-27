# Codex

Set `KLAREFI_API_KEY` in the environment Codex starts from, then run:

```sh
codex plugin marketplace add jmqcooper-ai/klarefi-mcp
codex plugin add klarefi@klarefi
```

Start a new session and enter `/mcp` to see the tools. The same config applies
to the Codex IDE extension. To remove it, run
`codex plugin remove klarefi@klarefi`.

Set the key before you start Codex. The plugin's server entry reads it from
the environment and does not start without it.

To add only the MCP server, merge [config.toml.example](config.toml.example)
into `~/.codex/config.toml`, or follow the
[Codex setup](https://www.klarefi.com/docs/api/connect-assistants#codex). Use
the plugin or the standalone entry, not both, so the server is not registered
twice.

[portable/](portable/) holds the same server in OpenAI's plugin package format,
with bearer API-key authentication. It has not been tested in an OpenAI host.
