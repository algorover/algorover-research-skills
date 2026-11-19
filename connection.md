# Connect AlgoRover Research

Install this Skill using `npx skills add algorover/algorover-research-skills --skill algorover-research`. Add the hosted MCP server separately in a client supporting Streamable HTTP and OAuth.

- Server name: `algorover-research`
- URL: `https://research.algorover.ai/mcp`
- Transport: Streamable HTTP
- Permissions for runs and reports: `research:read research:run`

For Cursor, add this entry to MCP settings while preserving other entries:

```json
{"mcpServers":{"algorover-research":{"url":"https://research.algorover.ai/mcp"}}}
```

For Gemini CLI, the corresponding server settings are:

```json
{"mcpServers":{"algorover-research":{"httpUrl":"https://research.algorover.ai/mcp","oauth":{"enabled":true,"scopes":["research:read","research:run"]}}}}
```

Use `/mcp auth algorover-research` inside Gemini CLI when authorization is required. For other hosts, use their MCP authorization interface. OAuth must complete in the browser and return successfully to the client.

Verify the connection by calling `search_strategies` with a supported locale. A skill installation alone does not establish an MCP connection or authorize personal research.

Privacy: https://www.algorover.ai/privacy/
Support: https://www.algorover.ai/en/help/
