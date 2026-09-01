# MCP Server Setup

This repo was created as a testing ground for configuring MCP (Model Context Protocol) servers in OpenCode.

## User Environment
- **OS**: Windows 10 Home (build 26200.6725, x64)
- **Storage**: ~40 GB free (cleaned up from ~30 GB)
- **Node**: v24.19.0, npx 12.0.2
- **Shell**: PowerShell 5.1

## Configured MCP Servers

### Context7 (Remote)
- URL: `https://mcp.context7.com/mcp`
- Purpose: Fetches real-time documentation for libraries/frameworks
- No auth needed

### Filesystem (Local via npx)
- Package: `@modelcontextprotocol/server-filesystem`
- Scope: `C:\Users\sophi`
- Purpose: Read, write, search, edit, move files locally
- No auth needed

### GitHub (Local via npx)
- Package: `@modelcontextprotocol/server-github` (deprecated but functional)
- Auth: GitHub PAT stored in config (never commit this!)
- Purpose: Issues, PRs, code search, repo management
- Config location: Project-level `opencode.json`

### Supabase (Remote)
- URL: `https://mcp.supabase.com/mcp`
- Auth: OAuth (requires `opencode mcp auth supabase` after restart)
- Config location: Global config `~/.config/opencode/opencode.jsonc`
- Purpose: Database queries, schema browsing, Edge Functions, logs

## Config Locations
- **Project config**: `C:\Users\sophi\opencode.json` — contains all MCP servers
- **Global config**: `C:\Users\sophi\.config\opencode\opencode.jsonc` — contains Supabase (needed for auth command to detect it)

## Pending Setup
1. **WSL2**: Ubuntu was downloading via `wsl --install`. Needs to complete and reboot.
2. **Docker Desktop**: Requires WSL2 on Windows 10 Home. Cannot install until WSL is working.
3. **Supabase OAuth**: Run `opencode mcp auth supabase` after restarting opencode.

## Storage Cleanup Performed
- npm cache: 5.2 GB
- Temp files: 433 MB
- ms-playwright: 701 MB
- Chrome OptGuideOnDeviceModel: 4 GB

## How to Use These MCP Servers
- "What's the latest way to use useEffect in React 19?" → Context7
- "Show me all files in my Documents folder" → Filesystem
- "What open issues do I have?" → GitHub
- "Show me the schema of my users table" → Supabase
- "Create an issue titled 'Fix login bug'" → GitHub
- "Check my Supabase schema, then write a Next.js API route using latest docs" → Combined

## Important Notes
- The GitHub MCP package (`@modelcontextprotocol/server-github`) is deprecated but still works
- Supabase MCP config MUST be in global config for the auth command to detect it
- Docker MCP does not exist as an official package — was deprioritized
- Never commit the GitHub PAT to any repo
