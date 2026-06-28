# Can You Connect Hostaway to Claude?

Source: https://rapideyeinspections.com/blog/can-you-connect-hostaway-to-claude/

_Yes. You connect Hostaway to Claude with a small, read-only MCP server you run yourself. Here is what's possible and how to set it up in about 20 minutes._

# Can you connect Hostaway to Claude?

**Yes.** You connect Hostaway to Claude by running a small **MCP server**: a lightweight program on your own computer that wraps the Hostaway Public API. Once it's connected, Claude Desktop or Claude Code can read your listings, reservations, calendar, and tasks and answer questions about them in plain English, no dashboards or exports.

MCP (the Model Context Protocol) is an open standard from Anthropic that lets AI assistants talk to outside systems. Hostaway has no official MCP server as of June 2026, so you build a focused one yourself. It's free, takes about 20 minutes, and the Hostaway Public API uses self-serve credentials, so you don't need to be a Marketplace partner.

The server is **read-only by default**, which means Claude can look at your data but cannot change reservations, pricing, or messages. Your credentials stay in environment variables on your own machine and the server runs locally, so nothing about your account is exposed to the outside world.

The full walkthrough has the working Node.js code, the Claude Desktop and Claude Code setup, and example prompts.

## Related

- [Can you connect Hostaway to ChatGPT?](https://rapideyeinspections.com/blog/can-you-connect-hostaway-to-chatgpt/)

- [Can you connect Hostaway to Gemini?](https://rapideyeinspections.com/blog/can-you-connect-hostaway-to-gemini/)

- [How do I use AI with Hostaway?](https://rapideyeinspections.com/blog/how-to-use-ai-with-hostaway/)

- [Does Hostaway have an MCP server?](https://rapideyeinspections.com/blog/does-hostaway-have-an-mcp-server/)

- [Can ChatGPT access my Hostaway data?](https://rapideyeinspections.com/blog/can-chatgpt-access-my-hostaway-data/)
