# Poolside (poolside-ai)

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

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/poolside-ai/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/poolside-ai/refs/heads/main/apis.yml)

## Does Poolside have a public API?

Not a self-serve one. This is a more nuanced case than most entries in this catalog:

- **Real, public API docs exist.** docs.poolside.ai publishes a full reference for an OpenAI-compatible inference API (`/openai/v1/chat/completions`, `/openai/v1/completions`, `/openai/v1/models`), an admin Identity Management API (`/poolside/v1`), and a SCIM 2.0 provisioning endpoint (`/scim`). A real OpenAPI 3.1 document is published at `https://api.poolsi.de/openai/openapi.json`.
- **There is no shared public host.** Poolside's own docs state the base URL is "configured per deployment: `https://<api-domain>`" - the fetched OpenAPI spec has no `servers` field for exactly this reason. Each customer gets their own domain once Poolside is deployed into their environment.
- **Access requires an existing deployment.** API key creation assumes "you can access your Poolside deployment" (developer keys) or a `tenant-admin` role (service-account keys). There is no public account-creation or API-key-purchase flow on poolside.ai.
- **No public pricing.** The poolside.ai site has no pricing or contact-sales link in its navigation; engagement is a direct sales conversation. Poolside's own `/enterprise` page describes delivery into a customer's AWS/Azure/Google Cloud VPC, on Poolside-pre-provisioned hardware, or on the customer's own NVIDIA GPU cluster via Helm - including fully air-gapped on-prem installs.
- **A public, third-party workaround exists.** Poolside's smaller open-weight model, Laguna XS 2.1, is listed on [OpenRouter](https://openrouter.ai/poolside) and callable through OpenRouter's own public API and pricing. That is a genuinely self-serve way to send a request to a Poolside model, but it is OpenRouter's endpoint and billing, not Poolside's.

## Type

- **x-type:** company

## Tags

- AI, LLM, Foundation Models, Agentic Coding, Software Engineering, Enterprise, On-Prem, Open Weights

## Timestamps

- **Created:** 2026-07-02
- **Modified:** 2026-07-02

## APIs

| API | Description |
|---|---|
| Poolside Chat Completions API | OpenAI-compatible chat completions (`POST /openai/v1/chat/completions`) serving Laguna models; base URL is per-deployment. |
| Poolside Completions API (Legacy) | Deprecated token-completion endpoint (`POST /openai/v1/completions`), still published in the OpenAPI spec. |
| Poolside Models API | Lists models available on a deployment (`GET /openai/v1/models`). |
| Poolside Identity Management API | Admin API (`/poolside/v1`) for user and team management, alternative/complement to SCIM. |
| Poolside SCIM API | SCIM 2.0 provisioning endpoint (`/scim`) for connecting an external identity provider. |

## Common Properties

- [GitHub Organization](https://github.com/poolsideai)
- [LinkedIn](https://www.linkedin.com/company/poolsideai)
- [Website](https://poolside.ai/)
- [Documentation](https://docs.poolside.ai/)
- [Plans](plans/poolside-ai-plans-pricing.yml) — API Commons Plans 0.1
- [Rate Limits](rate-limits/poolside-ai-rate-limits.yml) — API Commons Rate Limits 0.1
- [Fin Ops](finops/poolside-ai-finops.yml) — FOCUS-aligned FinOps Framework 1.0

## Artifacts

| Artifact | Path | Notes |
|---|---|---|
| OpenAPI | `openapi/poolside-ai-openapi.json` | Real spec fetched from `https://api.poolsi.de/openai/openapi.json` (OpenAPI 3.1.0, no `servers` field - per-deployment host). |
| Plans | `plans/poolside-ai-plans-pricing.yml` | No public price list; enterprise contract only, plus third-party OpenRouter usage pricing for Laguna XS 2.1. |
| Rate Limits | `rate-limits/poolside-ai-rate-limits.yml` | No published numeric limits; throughput is bound by the GPU capacity provisioned per deployment. |
| FinOps | `finops/poolside-ai-finops.yml` | No metered Poolside invoice; cost governance is contract + deployment-infrastructure spend. |
| Review | `review.yml` | "Does Poolside expose a documented public WebSocket API?" - answer: false, with full sourcing on the enterprise-gated API model. |

## Maintainers

**FN:** Kin Lane

**Email:** kin@apievangelist.com
