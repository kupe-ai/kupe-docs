# Kupe docs

Public API docs for Kupe (`https://docs.kupe.in`). Interactive Try it uses `openapi.yaml` (Bearer `sk-kupe-YOUR_KEY`). API host: `https://x.kupe.in`.

## Local preview

From this directory:

```bash
npx mintlify dev
```

Opens a local preview (usually [http://localhost:3000](http://localhost:3000)). Requires Node 18+.

```bash
npx mintlify dev --port 3333
```

Push to `main` to publish `docs.kupe.in` (connected docs host).

## Layout

| Path | Role |
| --- | --- |
| `docs.json` | Theme, nav, OpenAPI playground |
| `openapi.yaml` | Curated public OpenAPI |
| `kupe-mcp.mdx` | Kupe MCP install (`/kupe-mcp`) |
| `custom.css` | Brand matrix + MCP brand cards |
| `images/brands/` | Cursor / Claude / Codex logos |

## Note on `/mcp`

`https://docs.kupe.in/mcp` is reserved for the docs-search MCP endpoint (JSON). The human guide is **`/kupe-mcp`**. The Kupe platform MCP is **`http://mcp.kupe.in/mcp`**.
