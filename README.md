# Jobvetta

API Evangelist catalog entry for [Jobvetta](https://www.jobvetta.com) — live, vetted job openings
in India, gathered and checked against official employer sources. Available as a REST API and a
hosted MCP server that share one key.

| | |
|---|---|
| REST base | `https://api.jobvetta.com/v1` |
| Auth | Bearer token in the `Authorization` header |
| MCP | `https://api.jobvetta.com/mcp` — hosted, `tools/list` answers **unauthenticated** |
| Tools | `search_jobs` (q, location, days, limit) · `get_job` (job_id) |
| Scope | India only — non-Indian locations return no results |

Free during early access, with a shared limit of 50 tool calls per day and up to 20 jobs per
search across both surfaces.

## Recovered from the parked queue

The add-API pipeline parked this submission on 2026-07-24 at confidence 5, reason
`no_consumable_surface`. That was wrong — the API is live and enforcing auth, and the MCP server
is hosted and publicly discoverable. What is missing is an OpenAPI: the surface is documented in
HTML but not specified, and the gate could not see it. Tracked as
[roadmap#3](https://github.com/api-evangelist/roadmap/issues/3).

## Known gaps

- **No OpenAPI.** Nothing machine-readable to harvest or generate clients from. The highest-value
  thing they could add.
- **No `llms.txt`**, and no MCP server card at `/.well-known/mcp.json` despite the docs mentioning
  one. Discovery works through `tools/list` alone.

## This is a catalog entry, not Jobvetta

This repo is API Evangelist's profile *about* Jobvetta. For the product, an API key, or support,
go to [jobvetta.com](https://www.jobvetta.com).

If something here is wrong, open an issue on this repo or in the
[APIs.io Inbox](https://github.com/api-search/inbox).
