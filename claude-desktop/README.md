# Claude Desktop

[klarefi.mcpb](klarefi.mcpb) is a Claude Desktop extension. It runs the Klarefi
MCP server on your computer over stdio. The server calls the Klarefi API under
`https://www.klarefi.com/api/v1/`, and its tools cannot change that address.
When you upload a document, the file goes to the storage address the API
returns for that upload.

1. Download `klarefi.mcpb` and check its SHA-256:
   `14bba0e16bf0655005b0c65bdd657ac273e7e86191262b98cab80d6b0b709509`
   (`sha256sum klarefi.mcpb` on Linux, `shasum -a 256 klarefi.mcpb` on macOS).
2. Open it with Claude Desktop, review the extension and select **Install**.
3. For customer tools, enter your key in **Klarefi API key** in the extension
   settings. The setting is marked sensitive. Leave it blank if you only use
   applicant tools.

The extension was checked with the MCPB validator, and its server was run over
stdio outside Claude Desktop. Installing it in Claude Desktop has not been
tested.

You can also skip the extension and
[add Klarefi as a remote connector](https://www.klarefi.com/docs/api/connect-assistants#claude-web-and-remote-connectors).

## Licence

The archive holds Klarefi's code under the ISC licence in `LICENSE`. It also
bundles the MCP TypeScript SDK (Apache-2.0, with earlier contributions under
MIT), Zod (MIT), and libraries the SDK includes: Ajv, ajv-formats,
content-type, fast-deep-equal and json-schema-traverse (MIT), and fast-uri
(BSD-3-Clause). Their licence texts and copyright notices are in
`THIRD_PARTY_NOTICES.txt` inside the archive, and in
[THIRD_PARTY_NOTICES.txt](THIRD_PARTY_NOTICES.txt) here.
