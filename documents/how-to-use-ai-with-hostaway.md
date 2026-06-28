# How Do I Use AI With Hostaway?

Source: https://rapideyeinspections.com/blog/how-to-use-ai-with-hostaway/

_Connect Hostaway to your AI assistant with a small MCP server, then ask Claude, the Gemini CLI, or ChatGPT about your listings and reservations in plain English._

# How do I use AI with Hostaway?

You connect Hostaway to your AI assistant with a small **MCP server**: a local program that wraps the Hostaway Public API and exposes it as tools. Once connected, **Claude**, the **Gemini CLI**, or **ChatGPT** (via a hosted connector) can read your listings, reservations, calendar, and tasks and answer questions in plain English.

It's free, takes about 20 minutes, and is read-only by default, so the assistant can look but not change anything. The three steps are the same whichever assistant you use:

- **Get your API credentials.** In Hostaway, open Settings then Hostaway API and copy your Account ID and an API key. The Public API is self-serve, so no partner approval is needed.

- **Run the MCP server.** A small Node.js file wraps the API and exposes read-only tools for listings, reservations, calendar, and tasks.

- **Ask in plain English.** Point Claude, Gemini, or ChatGPT at the server and ask things like "what checks out tomorrow?" or "which listings have a gap next week?"

The full walkthrough has the working code and the exact setup for each assistant.

## Related

- [Can you connect Hostaway to Claude?](https://rapideyeinspections.com/blog/can-you-connect-hostaway-to-claude/)

- [Can you connect Hostaway to ChatGPT?](https://rapideyeinspections.com/blog/can-you-connect-hostaway-to-chatgpt/)

- [Can you connect Hostaway to Gemini?](https://rapideyeinspections.com/blog/can-you-connect-hostaway-to-gemini/)

- [Does Hostaway have an MCP server?](https://rapideyeinspections.com/blog/does-hostaway-have-an-mcp-server/)

- [Can ChatGPT access my Hostaway data?](https://rapideyeinspections.com/blog/can-chatgpt-access-my-hostaway-data/)
