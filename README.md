# Ulysses Docs

Public product documentation for [docs.tryulysses.com](https://docs.tryulysses.com), built with [Mintlify](https://mintlify.com).

| | |
|--|--|
| Site | https://docs.tryulysses.com |
| Mintlify URL | https://tryulysses.mintlify.site |
| Dashboard | https://app.mintlify.com |

## Local preview

Requires Node.js 20.17+.

```bash
npm i -g mint
mint dev
```

Preview at `http://localhost:3000`. Run `mint validate` before pushing.

## Publishing

Pushes to `main` deploy automatically via the Mintlify GitHub App. No separate Fly or CI deploy is required.

## Custom domain

`docs.tryulysses.com` is configured in Mintlify. DNS on Namecheap:

1. Verification **TXT** records (from the Mintlify custom-domain UI)
2. After both show verified: **CNAME** `docs` → `cname.mintlify.builders`

## AI tooling

- Install Mintlify’s writing skill: `npx skills add https://mintlify.com/docs`
- Admin MCP (edits / settings): `https://mcp.mintlify.com`
- Published docs expose `/llms.txt` for agents

Internal eng runbooks stay in `grand-harbor` — do not sync those here.
