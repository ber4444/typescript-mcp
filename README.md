# TypeScript MCP Project

This project implements a Model Context Protocol server using TypeScript.

## Getting Started

1. Build:
```bash
npm install
```

2. Add to `.vscode/mcp.json`:
```
{
	"servers": {
		"binance-ts-mcp": {
			"command": "npx",
			"args": [
				"-y",
				"/FULL_PATH_GOES_HERE/typescript_mcp"
			]
		}
	},
	"inputs": []
}
```

3. Type "what's the BTC price now" into Copilot, and you'll see it use this mcp to answer

4. Debug with ` npx @modelcontextprotocol/inspector node /home/presence/AndroidStudioProjects/mcp-course/typescript_mcp/src/binance_mcp.ts`

5. Optionally, publish it to npmjs.com
  - `npm login`
  - `npm publish`
  - results: https://www.npmjs.com/package/gaborb-binancemcp
  - the mcp will still run locally when using npmjs, but it will be downloaded
  - remotely running MCPs would mean going along the lines of https://github.com/cloudflare/ai/tree/main/demos/remote-mcp-auth0

## Tools, resources

This project has a tool that connects to the Binance API to give the price of a given crypto symbol.

MCP resources provide easy access to files, database tables, API results, e.g. this project writes MCP activity log to a file resource.

## Dependencies

- `@modelcontextprotocol/sdk`: Core MCP functionality
- `zod`: Runtime type checking
- `typescript`: Development dependency for TypeScript compilation
- `@types/node`: Type definitions for Node.js

