# runx

![runx wordmark](assets/wordmark.svg)

Search the public Runx skill catalog and inspect a skill's source and requirements from your agent client. This plugin connects to Runx's **hosted discovery MCP** at `https://api.runx.ai/mcp`. The hosted tools are `search_skills` and `get_skill`; both are read-only. Running a skill is a separate, local Runx operation with its own authority, approvals and receipt.

The plugin includes one guided [discovery skill](skills/runx-discovery/SKILL.md) and the current folded-R mark for marketplace cards. It does not install or invoke the Runx runtime, grant access to local files or providers, or mint a receipt.

## Connect now

Remote MCP clients can use this server configuration:

```json
{
  "mcpServers": {
    "runx": {
      "type": "http",
      "url": "https://api.runx.ai/mcp"
    }
  }
}
```

For Claude Code, `claude mcp add --transport http runx https://api.runx.ai/mcp` adds the same remote server. The host manifests and `.mcp.json` package it for Grok Build, Claude Code and Cursor. Root `plugin.json` and the Agent Plugins `mcp.json` supply portable ChatGPT/Codex metadata with unauthenticated, read-only hosted discovery. Public directory review is separate from this source package; no ChatGPT/Codex approval is claimed here.

To install and execute skills locally, follow the [Runx documentation](https://runx.ai/docs) and the [Runx source](https://github.com/runxhq/runx/tree/main/oss). The hosted discovery connection does not execute local skills.

## Support and terms

[Documentation](https://runx.ai/docs) · [Privacy](https://runx.ai/privacy) · [Terms](https://runx.ai/terms) · [Support](https://runx.ai/support) · `ask@runx.ai`

The plugin files are Apache-2.0. Runx OSS is Apache-2.0; the hosted service and Runx name are governed by their own terms.
