# Klarefi MCP

[Klarefi](https://www.klarefi.com) is an AI intake agent for lending,
insurance, legal and public-sector teams. It reads what applicants send in,
asks for anything missing and links each fact to its source. A person makes
the decision.

This repository holds the install packages for Klarefi's MCP server. The
Claude Code, Codex, Gemini CLI, Cursor and Grok Build packages connect to the
hosted server:

```text
https://www.klarefi.com/mcp
```

The Claude Desktop extension runs the server on your computer over stdio
instead. It calls the Klarefi API under `https://www.klarefi.com/api/v1/`, and
sends uploaded documents to the storage address the API returns for each
upload.

Customer tools need a Klarefi API key, sent as `Authorization: Bearer <key>`.
Create one in Klarefi under **Settings → Developers**. Start with a test key.

The server's applicant tools work from a signed intake URL and need no key.
The client packages here still ask for one: they send
`Authorization: Bearer ${KLAREFI_API_KEY}`, and Codex and the Cursor plugin
require the variable to be set. To use only applicant tools, add the server
without the `Authorization` header, as the
[setup guide](https://www.klarefi.com/docs/api/connect-assistants) shows.

## Install

| Assistant      | Package                                        | Guide                                                |
| -------------- | ---------------------------------------------- | ---------------------------------------------------- |
| Claude Code    | `.claude-plugin/` and `.mcp.json`              | [claude-code/README.md](claude-code/README.md)       |
| Codex          | `.codex-plugin/`, `.agents/plugins/`, `codex/` | [codex/README.md](codex/README.md)                   |
| Gemini CLI     | `gemini-extension.json`                        | [gemini-cli/README.md](gemini-cli/README.md)         |
| Claude Desktop | `claude-desktop/klarefi.mcpb`                  | [claude-desktop/README.md](claude-desktop/README.md) |
| Cursor         | `.cursor-plugin/` and `mcp.json`               | [cursor/README.md](cursor/README.md)                 |
| Grok Build     | `grok/config.toml.example`                     | [grok/README.md](grok/README.md)                     |

For other clients, and to add the server by hand, see the
[setup guide](https://www.klarefi.com/docs/api/connect-assistants).
`server.json` is the MCP Registry entry.

## What was tested

Four clients installed their package from this repository. Before they
connected, the installed copy was pointed at a local Klarefi test instance
through a proxy that checked the key. Each listed 21 tools and sent the test
key it was given.

- Claude Code 2.1.332: plugin installed from this repository's marketplace.
- Codex CLI 0.172.0: plugin installed from this repository's marketplace.
- Gemini CLI 0.71.1: extension installed from a clone of this repository.
  Installing straight from the GitHub URL failed in this Gemini CLI version
  with a git configuration error that is not specific to this extension.
- Grok Build 1.0.92: `grok/config.toml.example`, checked with
  `grok mcp doctor`.

The Claude Desktop extension was tested outside Claude Desktop. Its server was
run over stdio with network calls intercepted. It listed 21 tools and
addressed its API requests to `https://www.klarefi.com/api/v1/`, even with
another address set in its environment.

Not tested: installing the Claude Desktop extension in Claude Desktop, the
Cursor plugin, the Codex IDE extension, and hosted assistants such as ChatGPT,
Claude on the web, the Gemini app and Grok on the web.

## Licence

Klarefi's files are under the ISC licence in [LICENSE](LICENSE). The Claude
Desktop extension also bundles third-party code under its own licences; see
[claude-desktop/README.md](claude-desktop/README.md).

## Links

- [Documentation](https://www.klarefi.com/docs/guides/agent-intake)
- [Privacy](https://www.klarefi.com/privacy)
- [Terms](https://www.klarefi.com/terms)
- [Support](mailto:support@klarefi.com)
