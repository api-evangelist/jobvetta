# Jobvetta

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
