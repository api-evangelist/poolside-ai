# Poolside (poolside-ai)

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
