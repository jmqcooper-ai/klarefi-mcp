# Klarefi MCP

[Klarefi](https://www.klarefi.com) is an AI intake agent for lending,
insurance, legal and public-sector teams. It reads what applicants send in,
asks for anything missing and links each fact to its source. A person makes
the decision.

This repository holds the install packages for the hosted Klarefi MCP server.
Every package connects to the same endpoint:

```text
https://www.klarefi.com/mcp
```

Customer tools need a Klarefi API key, sent as `Authorization: Bearer <key>`.
Create one in Klarefi under **Settings → Developers**. Start with a test key.
Applicant tools work from a signed intake URL and need no key.

## Install

| Assistant      | Package                                                          | Guide                                          |
| -------------- | ---------------------------------------------------------------- | ---------------------------------------------- |
| Claude Code    | `.claude-plugin/` and `.mcp.json`                                | [claude-code/README.md](claude-code/README.md) |
| Codex          | `.codex-plugin/`, `.agents/plugins/` and `codex/`                | [codex/README.md](codex/README.md)             |
| Gemini CLI     | `gemini-extension.json`                                          | [gemini-cli/README.md](gemini-cli/README.md)   |
| Claude Desktop | `claude-desktop/klarefi.mcpb`                                    | [claude-desktop/README.md](claude-desktop/README.md) |
| Cursor         | `.cursor-plugin/` and `mcp.json`                                 | [cursor/README.md](cursor/README.md)           |
| Grok Build     | `grok/config.toml.example`                                       | [grok/README.md](grok/README.md)               |

For other clients, and to add the server by hand, see the
[setup guide](https://www.klarefi.com/docs/api/connect-assistants).
`server.json` is the MCP Registry entry.

## What was tested

Each package below was installed from this repository and pointed at a local
Klarefi test instance. Each listed 21 tools and sent the test key it was given.

- Claude Code 2.1.332: plugin installed from this repository's marketplace.
- Codex CLI 0.172.0: plugin installed from this repository's marketplace.
- Gemini CLI 0.71.1: extension installed from a clone of this repository.
  Installing straight from the GitHub URL failed in this Gemini CLI version
  with a git configuration error that is not specific to this extension.
- Grok Build 1.0.92: `grok/config.toml.example`, checked with
  `grok mcp doctor`.
- Claude Desktop: the bundle's server was run over stdio outside Claude
  Desktop. It listed 21 tools and addressed every request to
  `https://www.klarefi.com`, even with another address set in its
  environment.

Not tested: installing the Claude Desktop bundle in Claude Desktop, the Cursor
plugin, the Codex IDE extension, the OpenAI-format package in `codex/portable/`,
and hosted assistants such as ChatGPT, Claude on the web, the Gemini app and
Grok on the web.

## Links

- [Documentation](https://www.klarefi.com/docs/guides/agent-intake)
- [Privacy](https://www.klarefi.com/privacy)
- [Terms](https://www.klarefi.com/terms)
- [Support](mailto:support@klarefi.com)
