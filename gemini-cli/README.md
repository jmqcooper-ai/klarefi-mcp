# Gemini CLI

The extension manifest is [gemini-extension.json](../gemini-extension.json) at
the root of this repository. Install it with:

```sh
gemini extensions install https://github.com/jmqcooper-ai/klarefi-mcp
gemini mcp list
```

Approve the extension and enter your key at the **Klarefi API key** prompt.
The prompt hides what you type. In a session, enter `/mcp list` to
see the tools. To remove it, run `gemini extensions uninstall klarefi`.
