# Hatchet (hatchet)

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

Hatchet is an open-source distributed task queue and workflow orchestration engine for background jobs, AI agents, and durable workflows. It is Postgres-backed, MIT-licensed, and ships with first-class SDKs for Python, TypeScript, Go, and Ruby plus a managed offering (Hatchet Cloud) and a self-hostable engine (Docker Compose, Hatchet Lite, Helm chart). The platform separates the orchestration engine from worker execution so workers can run on the operator's own infrastructure (Kubernetes, ECS, Render, Railway, Porter, or any container platform).

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/hatchet/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/hatchet/refs/heads/main/apis.yml)

## Scope

- **Type:** Index

## Tags

- Task Queue
- Workflow Engine
- Durable Execution
- Background Tasks
- AI Agents
- Orchestration
- PostgreSQL
- Open Source

## Timestamps

- **Created:** 2026-03-27
- **Modified:** 2026-05-25

## APIs

### Hatchet API

The Hatchet REST API is the control plane for the Hatchet engine. It exposes operations for tasks, workflow runs, durable tasks, events, filters (CEL-based event routing), webhooks/webhook workers, tenants, users, workers, scheduled and cron workflows, alerting, rate limits, API tokens, observability (logs, traces, metrics), feature flags, and engine metadata. The contract is OpenAPI 3.1 and ships in-tree at hatchet-dev/hatchet under api-contracts/openapi. Stable endpoints are namespaced under /api/v1/stable; legacy endpoints remain under /api/v1. Authentication is bearer token or session cookie.

- **Human URL:** [https://docs.hatchet.run/](https://docs.hatchet.run/)
- **Base URL:** `https://api.hatchet-cloud.run`

#### Tags

- Task Queue
- Workflow Engine
- Durable Execution
- Background Tasks
- AI Agents
- Orchestration

#### Properties

- [Documentation](https://docs.hatchet.run/)
- [Getting Started](https://docs.hatchet.run/home/quickstart)
- [Quickstart](https://docs.hatchet.run/home/quickstart)
- [API Reference](https://docs.hatchet.run/)
- [OpenAPI](openapi/hatchet-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/hatchet.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/hatchet.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [OpenAPI](https://raw.githubusercontent.com/hatchet-dev/hatchet/main/api-contracts/openapi/openapi.yaml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [JSON Schema](json-schema/hatchet-v1-task-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/hatchet-v1-workflow-run-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/hatchet-v1-event-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/hatchet-v1-filter-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/hatchet-v1-webhook-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/hatchet-v1-task-event-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/hatchet-v1-log-line-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/hatchet-tenant-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/hatchet-worker-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/hatchet-rate-limit-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/hatchet-api-token-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/hatchet-workflow-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [Example](examples/v1-task-get-example.json)
- [Example](examples/v1-workflow-run-trigger-example.json)
- [Example](examples/v1-event-create-example.json)
- [Example](examples/v1-filter-create-example.json)
- [Example](examples/v1-task-cancel-example.json)
- [Example](examples/v1-task-replay-example.json)
- [Example](examples/v1-log-line-list-example.json)
- [Example](examples/rate-limit-upsert-example.json)
- [Example](examples/webhook-worker-create-example.json)
- [Example](examples/worker-list-example.json)
- [SDK](https://pypi.org/project/hatchet-sdk/)
- [SDK](https://www.npmjs.com/package/@hatchet-dev/typescript-sdk)
- [SDK](https://github.com/hatchet-dev/hatchet/tree/main/sdks/go)
- [SDK](https://github.com/hatchet-dev/hatchet/tree/main/sdks/ruby)
- [Code Examples](https://github.com/hatchet-dev/hatchet-python-quickstart)
- [Code Examples](https://github.com/hatchet-dev/hatchet-typescript-quickstart)
- [Code Examples](https://github.com/hatchet-dev/hatchet-go-quickstart)
- [Code Examples](https://github.com/hatchet-dev/hatchet-typescript-deep-research)
- [Code Examples](https://github.com/hatchet-dev/hatchet-typescript-code-agent)
- [Code Examples](https://github.com/hatchet-dev/hatchet-infra-examples)
- [Authentication](https://docs.hatchet.run/)
- [Rate Limits](rate-limits/hatchet-rate-limits.yml)
- [Self Hosting](https://docs.hatchet.run/self-hosting)
- [Source Code](https://github.com/hatchet-dev/hatchet)

## Common Properties

- [Website](https://hatchet.run/)
- [Documentation](https://docs.hatchet.run/)
- [L L Ms Txt](https://docs.hatchet.run/llms.txt)
- [Pricing](https://hatchet.run/pricing)
- [Plans](plans/hatchet-plans-pricing.yml)
- [Blog](https://hatchet.run/blog)
- [GitHub Organization](https://github.com/hatchet-dev)
- [GitHub Repository](https://github.com/hatchet-dev/hatchet)
- [Source Code](https://github.com/hatchet-dev/hatchet)
- [LinkedIn](https://www.linkedin.com/company/hatchet-run)
- [C L I](https://install.hatchet.run/install.sh)
- [Tools](https://github.com/hatchet-dev/homebrew-hatchet)
- [Tools](https://github.com/hatchet-dev/hatchet-charts)
- [Tools](https://github.com/hatchet-dev/terraform-provider-hatchet)
- [Tools](https://github.com/hatchet-dev/pgoutbox)
- [Tools](https://github.com/hatchet-dev/s3-batch-object-store)
- [Tools](https://github.com/hatchet-dev/buffered)
- [Tools](https://github.com/hatchet-dev/timediff)
- [Tutorials](https://github.com/hatchet-dev/hatchet-infra-examples)
- [Spectral Rules](rules/hatchet-rules.yml)
- [Vocabulary](vocabulary/hatchet-vocabulary.yml)
- [JSON-LD](json-ld/hatchet-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [Compliance](https://hatchet.run/pricing)
- [Features](undefined)
- [Use Cases](undefined)
- [Integrations](undefined)
- [Solutions](undefined)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
