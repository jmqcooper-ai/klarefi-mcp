# Gemini CLI

The extension manifest is [gemini-extension.json](../gemini-extension.json) at
the root of this repository. Clone the repository and install from the folder:

```sh
git clone https://github.com/jmqcooper-ai/klarefi-mcp
gemini extensions install ./klarefi-mcp
gemini mcp list
```

Gemini CLI asks whether to trust the cloned folder; answer `y` to continue.
Approve the extension and enter your key at the **Klarefi API key** prompt.
The prompt masks the key. In a session, enter `/mcp list` to see the tools. To
remove it, run `gemini extensions uninstall klarefi`.

Where your Gemini CLI version can install from a URL, this also works:

```sh
gemini extensions install https://github.com/jmqcooper-ai/klarefi-mcp
```

Gemini CLI 0.71.1 fails that command with a `GIT_CONFIG_SYSTEM` error for any
repository, so use the clone above with that version.
