# Kupe docs

Mintlify site for the public Kupe API (`https://x.kupe.in`). Interactive Try it uses `openapi.yaml` (Bearer `sk-kupe-YOUR_KEY`).

## Local preview

From this directory:

```bash
npx mintlify dev
```

Opens a local preview (usually [http://localhost:3000](http://localhost:3000)). Requires Node 18+. First run downloads the Mintlify CLI.

```bash
npx mintlify dev --port 3333
```

Do not deploy from this repo unless you intend to publish to Mintlify cloud / `docs.kupe.in`.

## Layout

| Path | Role |
| --- | --- |
| `docs.json` | Theme, nav, OpenAPI playground |
| `openapi.yaml` | Curated public spec (no payments, internal, or per-service usage) |
| `custom.css` | Satoshi + CSS dot-matrix hero |
| `logo/` | Wordmarks and mark copied from `kupe-frontend/public/brand` |
| `fonts/` | Satoshi woff2 (same Fontshare files the frontend loads from CDN) |

## Refresh OpenAPI

Dump FastAPI, strip excluded paths, write YAML (run from `kupe-backend` with that package on `PYTHONPATH`):

```bash
python3 -c "from app.openapi_public import build_public_openapi; ..."
```

Keep exclusions aligned with `kupe-backend/app/openapi_public.py`.
