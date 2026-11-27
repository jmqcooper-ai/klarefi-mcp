# Cursor

[.cursor-plugin/plugin.json](../.cursor-plugin/plugin.json) is the Cursor plugin
manifest. It points at [mcp.json](../mcp.json) and asks for your key as the
`KLAREFI_API_KEY` variable.

To add the server without the plugin, merge this into `~/.cursor/mcp.json` and
set `KLAREFI_API_KEY` in Cursor's environment:

```json
{
  "mcpServers": {
    "klarefi": {
      "url": "https://www.klarefi.com/mcp",
      "headers": { "Authorization": "Bearer ${env:KLAREFI_API_KEY}" }
    }
  }
}
```

The [setup guide](https://www.klarefi.com/docs/api/connect-assistants) has a
Cursor install link. Neither the plugin nor the config has been tested in
Cursor.
