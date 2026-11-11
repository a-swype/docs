# Fissient docs

Developer documentation for the Fissient API, published with [Mintlify](https://mintlify.com) from the `main` branch.

## Layout

| Path | What it holds |
| --- | --- |
| `docs.json` | Site configuration and navigation |
| `index.mdx`, `quickstart.mdx` | Landing page and first-trade walkthrough |
| `concepts/` | The objects and rules of the API |
| `guides/` | Task-focused how-to guides |
| `agents/` | The MCP server for AI agents |
| `api-reference/` | One page per endpoint |

## Preview locally

```bash
npx mint@latest dev
```

Then open http://localhost:3000.

## Check before pushing

```bash
npx mint@latest broken-links
```

Writing conventions are in [AGENTS.md](AGENTS.md).
