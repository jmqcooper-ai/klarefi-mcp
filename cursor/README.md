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

For a team on Teams or Enterprise, Cursor documents adding a repository under
**Dashboard → Plugins & MCPs → Team Marketplaces → Add Marketplace → Import
from Repo**, after which team members install from **Customize**. This
repository has no Cursor marketplace file, and this route has not been tested.

## Set the key

The plugin stores no key. For a team install, Cursor's documentation has a
team admin set `KLAREFI_API_KEY` in the dashboard under **Plugins**, when
installing or later with **Configure** on the plugin.

Cursor's documentation does not say how a personal install from the local
plugin folder supplies a plugin variable. For a personal setup, use the config
below instead: it reads `KLAREFI_API_KEY` from Cursor's environment.

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
