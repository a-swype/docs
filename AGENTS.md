# Documentation project instructions

## About this project

- Developer documentation for Fissient, an invest-and-earn API for fintechs, wallets and AI agents.
- Built on [Mintlify](https://mintlify.com). Pages are MDX files with YAML frontmatter. Configuration lives in `docs.json`.
- `Guides` tab: concepts and how-to guides. `API reference` tab: one hand-written page per endpoint, using the `api:` frontmatter field.

## The rule that decides most questions

**Technical on the backend, never technical for the reader.** The API exposes users, dollars, instruments, quotes, orders and portfolios. The docs must do the same.

- Don't name the venues, issuers' token symbols, routing providers, wallet providers or networks an order uses internally. A user buys "NVIDIA" or "Dollar Savings".
- Networks appear only where the integrator has to choose one: deposit addresses, withdrawals and linked wallets.
- Never hide real risk, real fees or real failure. Say what happened in plain words.
- Never tell a reader an order is done unless its status is `completed`.

## Terminology

- "user", not "end user" or "customer account"
- "instrument" for anything in the catalog; "asset" only for what search returns
- "cash" or "cash balance" for uninvested money
- "guardrails" for the per-user `policy`
- "secret key", "agent key", "read-only key"
- "sandbox" and "live" for the two modes
- "linked wallet" for `linked_home_wallet`
- The product name appears as "Fissient". Use it sparingly so a rename is a small change; prefer "the API".

## Style

- Active voice, second person ("you").
- Sentence case for headings.
- One idea per sentence. Short paragraphs.
- Every endpoint page has a request example and a response example taken from real sandbox output, trimmed to the documented fields.
- Amounts in examples are decimal strings, as the API returns them.
- No em dashes.

## Content boundaries

- Document only the partner-facing API and the MCP server.
- Don't document the admin API, internal services or deployment.
- Don't document fields that reveal how an order was fulfilled.
