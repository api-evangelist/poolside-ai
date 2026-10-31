# Poolside

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
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Poolside is an AI foundation model lab (founded 2023 by former GitHub CTO Jason Warner and Eiso Kant) building open-weight foundation models - the Laguna family - purpose-built for agentic software engineering. Poolside does not run a shared public SaaS API the way OpenAI or Groq do. Instead it publishes a full, public API reference (docs.poolside.ai) for an OpenAI-compatible inference API plus an admin/identity API, but the API itself only comes alive once a customer has a provisioned Poolside deployment - into their own AWS/Azure/Google Cloud VPC, on customer-owned NVIDIA GPU clusters via Helm, or fully air-gapped on-prem. There is no public signup page, free tier, or published pricing; access is arranged directly with Poolside's sales team. Separately, Poolside's smaller open-weight model, Laguna XS 2.1, can be called by anyone through third-party inference hosts such as OpenRouter, which is the closest thing to a public, self-serve way to hit a Poolside model over HTTP.

**Areas:** Artificial Intelligence · LLM · Foundation Models · Agentic Coding · Software Engineering · Enterprise · On-Prem · Open Weights

## Poolside on APIs.io

Everything profiled for Poolside is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/poolside-ai/](https://apis.io/providers/poolside-ai/)** — or go straight to one of the APIs or properties below.

### APIs (4)

- [Poolside Identity Management API](https://apis.io/apis/poolside-ai/poolside-identity-management-api/) — Poolside's own admin API (/poolside/v1) for automating user and team administration on a deployment - create/get/update/delete users, and add, remove, or…
- [Poolside SCIM API](https://apis.io/apis/poolside-ai/poolside-scim-api/) — SCIM 2.0 provisioning endpoint (/scim) for connecting an external identity provider (Okta, Entra ID, etc.) to automatically provision and deprovision…
- [Poolside Chat API](https://apis.io/apis/poolside-ai/poolside-ai-chat-api/) — The chat API from Poolside — 2 operation(s) for chat.
- [Poolside Models API](https://apis.io/apis/poolside-ai/poolside-ai-models-api/) — The models API from Poolside — 1 operation(s) for models.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Poolside Ai Agentic Access](https://apis.io/agentic-access/poolside-ai/poolside-ai-agentic-access/)

#### Collections (2)

Postman and Open Collection request collections.

- [OpenAI Compatible chat API](https://apis.io/collections/poolside-ai/open-poolside-ai-chat-api/)
- [OpenAI Compatible chat models API](https://apis.io/collections/poolside-ai/open-poolside-ai-models-api/)

#### Security (3)

Authentication, trust centre, and vulnerability disclosure.

- [Poolside Ai Authentication](https://apis.io/security/poolside-ai/poolside-ai-authentication/)
- [Poolside Ai Trust Center](https://apis.io/security/poolside-ai/poolside-ai-trust-center/)
- [Poolside Ai Vulnerability Disclosure](https://apis.io/security/poolside-ai/poolside-ai-vulnerability-disclosure/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Poolside Ai Plans Pricing](https://apis.io/plans/poolside-ai/poolside-ai-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Poolside Ai Rate Limits](https://apis.io/rate-limits/poolside-ai/poolside-ai-rate-limits/)

#### FinOps (1)

What the API costs to run, by operation.

- [Poolside Ai Finops](https://apis.io/finops/poolside-ai/poolside-ai-finops/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://poolside.ai/)
- [Documentation](https://docs.poolside.ai/)
- [Blog](https://poolside.ai/blog)
- [GitHub](https://github.com/poolsideai)

## API Evangelist rating

**Kin Score 25.3** — emerging · rubric 0.24.0 · scored 2026-10-17

| Facet | Score |
|---|---|
| Discoverability | 66.1 |
| Contract quality | 41.9 |
| Contract governance | 0.0 |
| Operational transparency | 10.5 |
| Developer ergonomics | 23.8 |
| Access clarity | 15.8 |

**Agent readiness 23.7** — agent-aware

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | — |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | verified |
| OpenAPI Examples | — |
| Rate Limit Signal | derived (partial credit) |
| Event Surface Described | — |
| Agent Skills | — |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |

**Regulatory alignment 15.5** — AI & Biometrics

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/poolside-ai/](https://apis.io/providers/poolside-ai/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Poolside: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/poolside-ai/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
