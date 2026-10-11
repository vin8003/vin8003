# OmniRoute plugin

Claude Code plugin for [OmniRoute](https://github.com/diegosouzapw/OmniRoute), the unified AI proxy/router.

- **Skills** (`skills/`): 46 skills copied from `skills/` in the OmniRoute repo (version 3.8.52, MIT). Re-copy them when OmniRoute is upgraded.
- **MCP server** (`.mcp.json`): starts OmniRoute's MCP server over stdio with `npx -y omniroute@3.8.52 --mcp`. It needs Node.js 22.22.2 or newer (below 23), or 24.0.0 or newer (below 27). It runs against a local OmniRoute data directory (`~/.omniroute/` by default).

To use a running OmniRoute instance over HTTP instead, replace the stdio entry with:

```bash
claude mcp add-server omniroute --type http --url http://localhost:20128/api/mcp/stream
```

License: MIT, as in the upstream repo's `LICENSE`.
