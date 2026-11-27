# Grok Build

Merge [config.toml.example](config.toml.example) into `~/.grok/config.toml`,
set `KLAREFI_API_KEY` in the environment, then run:

```sh
grok mcp doctor klarefi
```

Open `/mcps` in a session to see the server. If `KLAREFI_API_KEY` is unset,
the server can still report healthy because listing tools needs no key, but
customer tools fail.

See the [Grok setup](https://www.klarefi.com/docs/api/connect-assistants#grok-build)
for more.
