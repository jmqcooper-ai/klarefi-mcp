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

Being filled in from the install tests on this branch.

## Links

- [Documentation](https://www.klarefi.com/docs/guides/agent-intake)
- [Privacy](https://www.klarefi.com/privacy)
- [Terms](https://www.klarefi.com/terms)
- [Support](mailto:support@klarefi.com)
