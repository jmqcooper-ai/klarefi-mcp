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

Klarefi uses a fixed API key sent as a bearer token. OpenAI's plugin
submission portal cannot complete connection setup with a fixed bearer token,
so this package is for direct installs, not a directory listing.
