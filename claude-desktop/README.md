# Claude Desktop

[klarefi.mcpb](klarefi.mcpb) is a Claude Desktop extension. It runs the Klarefi
MCP server on your computer and always sends requests to
`https://www.klarefi.com`. Its tools cannot change that address.

1. Download `klarefi.mcpb`.
2. Open it with Claude Desktop, review the extension and select **Install**.
3. For customer tools, enter your key in **Klarefi API key** in the extension
   settings. The setting is marked sensitive. Leave it blank if you only use
   applicant tools.

The bundle was checked with the MCPB validator and its server was run over
stdio outside Claude Desktop. Installing it in Claude Desktop has not been
tested.

You can also skip the extension and
[add Klarefi as a remote connector](https://www.klarefi.com/docs/api/connect-assistants#claude-web-and-remote-connectors).

The bundle is licensed under the ISC licence in [LICENSE](../LICENSE), which
the archive also contains.
