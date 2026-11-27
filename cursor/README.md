# Cursor

[.cursor-plugin/plugin.json](../.cursor-plugin/plugin.json) is the Cursor plugin
manifest. It uses [mcp.json](../mcp.json) and declares `KLAREFI_API_KEY` as a
plugin variable.

## Install the plugin

For yourself, clone the repository into Cursor's local plugin folder, then
restart Cursor or run **Developer: Reload Window**:

```sh
git clone https://github.com/jmqcooper-ai/klarefi-mcp ~/.cursor/plugins/local/klarefi
```

On Enterprise plans, local plugins need **Allow Local Plugin Imports** under
**Dashboard → Settings → Security & Identity → Marketplace and Plugins**.

For a team on Teams or Enterprise, an admin can add this repository under
**Dashboard → Plugins & MCPs → Team Marketplaces → Add Marketplace → Import
from Repo**. Team members then install Klarefi from **Customize**.

## Set the key

The plugin stores no key. A team admin sets `KLAREFI_API_KEY` in the dashboard
under **Plugins**, when installing or later with **Configure** on the plugin.

## Without the plugin

Merge this into `~/.cursor/mcp.json` and set `KLAREFI_API_KEY` in Cursor's
environment:

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
Cursor install link. Neither the plugin nor this config has been tested in
Cursor.
