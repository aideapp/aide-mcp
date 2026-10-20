# Aide MCP

Connect your AI agent to [Aide](https://aide.app), the AI customer service platform: search your
knowledge base, look up Shopify orders, and find, read, note, reply to and update support
conversations, as yourself and within your role in Aide.

This repository holds install metadata only. The server is hosted by Aide at
`https://app-api.aide.app/mcp` (streamable HTTP). You sign in with your Aide account through
OAuth; there is no API key to configure. Requires an Aide account.

## Cursor

Install **Aide** from the Cursor Marketplace, or:

[![Add Aide to Cursor](https://cursor.com/deeplink/mcp-install-dark.png)](https://cursor.com/link/mcp/install?name=aide&config=eyJ1cmwiOiJodHRwczovL2FwcC1hcGkuYWlkZS5hcHAvbWNwIn0=)

Or add to `~/.cursor/mcp.json`:

```json
{ "mcpServers": { "aide": { "url": "https://app-api.aide.app/mcp" } } }
```

## Gemini CLI

```bash
gemini extensions install https://github.com/aideapp/aide-mcp
```

Start `gemini` and sign in when prompted, or run `/mcp auth aide`.

## VS Code

```bash
code --add-mcp '{"name":"aide","type":"http","url":"https://app-api.aide.app/mcp"}'
```

## Claude Code

```bash
claude mcp add --transport http aide https://app-api.aide.app/mcp
```

Then run `/mcp` in Claude Code to sign in.

## Codex

Add to `~/.codex/config.toml`:

```toml
[mcp_servers.aide]
url = "https://app-api.aide.app/mcp"
```

Then run `codex mcp login aide`.

## Claude and ChatGPT

Add `https://app-api.aide.app/mcp` as a custom connector and sign in with your Aide account.

## Access and data

Connected apps see only what you can see in Aide, and every action is recorded as you. Refunds
and cancellations above your approval limits wait for an admin. Disconnect an app at any time in
Aide under Settings > Developers.

Support: support@aide.app · [Privacy](https://aide.app/privacy) · [Terms](https://aide.app/terms)

## License

The files in this repository are MIT licensed. The Aide service, name and logo are not covered by
this license.
