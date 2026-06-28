# Does Hostaway Have an MCP Server?

Source: https://rapideyeinspections.com/blog/does-hostaway-have-an-mcp-server/

_Not an official one as of June 2026. Hostaway has a Public API but no first-party MCP server, so you build a focused read-only one yourself in about 20 minutes._

# Does Hostaway have an MCP server?

**Not an official one, as of June 2026.** Hostaway publishes a Public API but no first-party MCP server. You can build a focused, **read-only** MCP server yourself in about 20 minutes (our guide has the working code), or use a no-code bridge like Zapier MCP.

An MCP (Model Context Protocol) server is a small program that exposes one system's data to AI assistants as a set of tools. Because there's no first-party Hostaway server, building your own is actually an advantage: you decide exactly what the assistant can see, and you can keep it read-only so it can never change a reservation or price.

The Hostaway Public API uses self-serve credentials you generate under Settings, so you don't need to be a Marketplace partner to build against it. The same server then works with Claude, the Gemini CLI, and (when hosted) ChatGPT.

The full guide has the Node.js code, the setup, and example prompts to try.

## Related

- [Can you connect Hostaway to Claude?](https://rapideyeinspections.com/blog/can-you-connect-hostaway-to-claude/)

- [Can you connect Hostaway to ChatGPT?](https://rapideyeinspections.com/blog/can-you-connect-hostaway-to-chatgpt/)

- [Can you connect Hostaway to Gemini?](https://rapideyeinspections.com/blog/can-you-connect-hostaway-to-gemini/)

- [How do I use AI with Hostaway?](https://rapideyeinspections.com/blog/how-to-use-ai-with-hostaway/)

- [Can ChatGPT access my Hostaway data?](https://rapideyeinspections.com/blog/can-chatgpt-access-my-hostaway-data/)
