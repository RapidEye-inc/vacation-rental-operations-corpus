# Can You Connect Hostaway to Gemini?

Source: https://rapideyeinspections.com/blog/can-you-connect-hostaway-to-gemini/

_Yes. The Gemini CLI supports MCP via gemini mcp add, so the same local Hostaway MCP server you build for Claude works with Gemini unchanged. Here's how._

# Can you connect Hostaway to Gemini?

**Yes.** The Gemini CLI supports MCP servers through the gemini mcp add command, the same way Claude Code does, so the local Hostaway MCP server you build works with Gemini with no changes. Point it at the same index.js and ask Gemini about your listings, reservations, calendar, and tasks.

The Gemini CLI reads MCP servers from ~/.gemini/settings.json and supports both local (stdio) and remote (HTTP) servers. Because the Hostaway server in our guide runs locally over stdio, it drops straight into Gemini's config, no hosting or rewriting required.

As with Claude, the server is read-only by default, so Gemini can read your Hostaway data but cannot change anything, and your Public API credentials stay on your own machine.

Build the server once with the full guide, then add it to Claude Code or the Gemini CLI with one command each.

## Related

- [Can you connect Hostaway to Claude?](https://rapideyeinspections.com/blog/can-you-connect-hostaway-to-claude/)

- [Can you connect Hostaway to ChatGPT?](https://rapideyeinspections.com/blog/can-you-connect-hostaway-to-chatgpt/)

- [How do I use AI with Hostaway?](https://rapideyeinspections.com/blog/how-to-use-ai-with-hostaway/)

- [Does Hostaway have an MCP server?](https://rapideyeinspections.com/blog/does-hostaway-have-an-mcp-server/)

- [Can ChatGPT access my Hostaway data?](https://rapideyeinspections.com/blog/can-chatgpt-access-my-hostaway-data/)
