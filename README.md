# Hatchet (hatchet)

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
