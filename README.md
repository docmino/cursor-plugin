# Docmino for Cursor

Create and edit interactive guides, lessons, forms, and client plans from Cursor. Search documents, work with nested pages, organize projects, and publish or share guides through your Docmino account.

This package connects to Docmino's hosted MCP server and includes a skill for working with its documents. It contains no local executable or backend source.

## Connect

You need a Docmino account and a Cursor version with remote MCP support.

For a local plugin preview, place this repository's contents in `~/.cursor/plugins/local/docmino`, then open Cursor's Customize page and connect the Docmino MCP server. Sign in to Docmino and review the permissions requested on the consent screen.

You can also connect just the server by adding this entry to `.cursor/mcp.json` in a project, or to `~/.cursor/mcp.json` for your user:

```json
{
  "mcpServers": {
    "docmino": {
      "url": "https://mcp.docmino.com/mcp"
    }
  }
}
```

The manual MCP connection provides the tools. Installing the plugin also provides the document-authoring skill. No API key or shared client secret belongs in this configuration; each person authenticates through Docmino's OAuth flow.

## Try it

- "Create a private onboarding guide with a Getting started page and a nested checklist."
- "Find my training guide and summarize it with a link."
- "Add a troubleshooting section to my guide, keeping all existing pages."
- "Create an interactive lesson with practice questions."
- "Open my guide so I can edit it."

The embedded editor requires an MCP Apps-capable client. When it is unavailable, use the document tools or open the returned Docmino link.

## Permissions and data

Actions are limited by your existing Docmino permissions and the scopes you grant. Relevant document, page, project, and sharing data can be returned to Cursor when its agent calls the tools. Review tool calls before approving changes, publishing, sharing, moving content between audiences, or deletion.

Revoke Docmino access in **Docmino Settings → Connected apps**. Cursor's processing of returned information is governed by Cursor's policies.

The integration does not process payments, upload new media, manage billing or organization memberships, retrieve form responses or comments, or invoke Docmino's internal AI assistant. Use the normal Docmino application for those tasks.

## Links

- [Docmino](https://docmino.com)
- [Documentation](https://docmino.com/documentation)
- [Support](https://docmino.com/docmino/contact)
- [Privacy policy](https://docmino.com/docmino/privacy)
- [Terms of service](https://docmino.com/docmino/terms)
- [Official MCP Registry entry](https://registry.modelcontextprotocol.io/v0.1/servers?search=io.github.docmino%2Fdocmino)

Published by Docmino Inc. Contact: hello@docmino.com.
