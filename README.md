# Hatchet (hatchet)

Hatchet is an open-source distributed task queue and workflow orchestration engine for background jobs, AI agents, and durable workflows. It is Postgres-backed, MIT-licensed, and ships with first-class SDKs for Python, TypeScript, Go, and Ruby plus a managed offering (Hatchet Cloud) and a self-hostable engine (Docker Compose, Hatchet Lite, Helm chart). The platform separates the orchestration engine from worker execution so workers can run on the operator's own infrastructure (Kubernetes, ECS, Render, Railway, Porter, or any container platform).

**URL:** [Visit APIs.json URL](https://raw.githubusercontent.com/api-evangelist/hatchet/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Tags

- Task Queue, Workflow Engine, Durable Execution, Background Tasks, AI Agents, Orchestration, PostgreSQL, Open Source

## Timestamps

- **Created:** 2026-03-27
- **Modified:** 2026-05-25

## APIs

### Hatchet API

The Hatchet REST API is the control plane for the Hatchet engine. It exposes operations for tasks, workflow runs, durable tasks, events, filters (CEL-based event routing), webhooks/webhook workers, tenants, users, workers, scheduled and cron workflows, alerting, rate limits, API tokens, observability (logs, traces, metrics), feature flags, and engine metadata. The contract is OpenAPI 3.1 and ships in-tree at hatchet-dev/hatchet under api-contracts/openapi. Stable endpoints are namespaced under `/api/v1/stable`; legacy endpoints remain under `/api/v1`. Authentication is bearer token or session cookie.

**Human URL:** [https://docs.hatchet.run/](https://docs.hatchet.run/)

#### Tags

- Task Queue, Workflow Engine, Durable Execution, Background Tasks, AI Agents, Orchestration

#### Properties

- [Documentation](https://docs.hatchet.run/)
- [Getting Started](https://docs.hatchet.run/home/quickstart)
- [Quickstart](https://docs.hatchet.run/home/quickstart)
- [API Reference](https://docs.hatchet.run/)
- [OpenAPI](openapi/hatchet-openapi.yml)
- [OpenAPI (canonical, $ref-composed)](https://raw.githubusercontent.com/hatchet-dev/hatchet/main/api-contracts/openapi/openapi.yaml)
- [Python SDK (PyPI)](https://pypi.org/project/hatchet-sdk/)
- [TypeScript SDK (npm)](https://www.npmjs.com/package/@hatchet-dev/typescript-sdk)
- [Go SDK](https://github.com/hatchet-dev/hatchet/tree/main/sdks/go)
- [Ruby SDK](https://github.com/hatchet-dev/hatchet/tree/main/sdks/ruby)
- [Python Quickstart](https://github.com/hatchet-dev/hatchet-python-quickstart)
- [TypeScript Quickstart](https://github.com/hatchet-dev/hatchet-typescript-quickstart)
- [Go Quickstart](https://github.com/hatchet-dev/hatchet-go-quickstart)
- [Deep Research Agent Pattern (TS)](https://github.com/hatchet-dev/hatchet-typescript-deep-research)
- [Coding Agent Pattern (TS)](https://github.com/hatchet-dev/hatchet-typescript-code-agent)
- [Worker Infrastructure Walkthroughs](https://github.com/hatchet-dev/hatchet-infra-examples)
- [Authentication (Bearer + Cookie)](https://docs.hatchet.run/)
- [Rate Limits](rate-limits/hatchet-rate-limits.yml)
- [Self Hosting](https://docs.hatchet.run/self-hosting)
- [Source Code](https://github.com/hatchet-dev/hatchet)

## Common Properties

- [Website](https://hatchet.run/)
- [Documentation](https://docs.hatchet.run/)
- [LLMs.txt](https://docs.hatchet.run/llms.txt)
- [Pricing](https://hatchet.run/pricing)
- [Plans (machine-readable)](plans/hatchet-plans-pricing.yml)
- [Blog](https://hatchet.run/blog)
- [GitHub Organization](https://github.com/hatchet-dev)
- [GitHub Repository (hatchet-dev/hatchet)](https://github.com/hatchet-dev/hatchet)
- [LinkedIn](https://www.linkedin.com/company/hatchet-run)
- [CLI installer](https://install.hatchet.run/install.sh)
- [Homebrew Tap](https://github.com/hatchet-dev/homebrew-hatchet)
- [Helm Chart](https://github.com/hatchet-dev/hatchet-charts)
- [Terraform Provider](https://github.com/hatchet-dev/terraform-provider-hatchet)
- [Compliance (SOC 2 / HIPAA)](https://hatchet.run/pricing)

## Features

| Name | Description |
|------|-------------|
| Durable Execution | Task and workflow state is persisted to Postgres so executions survive worker restarts, network partitions, and engine upgrades. |
| Low-Latency Scheduling | Sub-20ms task start times with intelligent assignment rules. |
| Code-First SDKs | Native language SDKs for Python, TypeScript, Go, and Ruby; tasks are versionable, testable functions. |
| Engine / Worker Separation | The orchestration engine and workers are decoupled; workers run on the customer's own infrastructure. |
| Postgres-Backed | Hatchet's only hard dependency is PostgreSQL; RabbitMQ is optional for higher-throughput deployments. |
| First-Class Rate Limits | Engine-level rate-limit primitive throttles task execution by named key, scope, and window — independent of HTTP rate limits. |
| CEL Event Filters | Common Expression Language filters bind incoming events to workflows with payload predicates. |
| Scheduled and Cron Workflows | One-shot scheduled runs and recurring cron-triggered workflows are first-class engine resources. |
| Webhook Workers | External HTTPS endpoints can be registered as workers; the engine delivers task runs as signed webhook requests. |
| OpenTelemetry Tracing | Workflows and tasks emit OTel traces; the engine exposes a trace lookup endpoint. |
| Replays and Restores | Failed or cancelled tasks can be replayed with the same input or restored to the run queue. |
| Multi-Tenant | Tenants isolate workflows, tasks, workers, and tokens; quotas and throughput are scoped per tenant. |
| Dashboard | Built-in web dashboard for inspecting runs, replaying tasks, and managing tenants. |
| Slack and SNS Alerting | Alerts can be dispatched to Slack channels or AWS SNS topics for ops escalation. |
| MIT-Licensed | Engine, API, SDKs, dashboard, and Helm chart are all MIT-licensed. |

## Use Cases

| Name | Description |
|------|-------------|
| AI Agent Orchestration | Manage tool calls, conversation state, timeouts, and checkpointing for production AI agents. |
| Background Jobs | Classic distributed task-queue use case — replace Celery, Sidekiq, BullMQ, or RQ with durable equivalents. |
| Durable Workflows | Multi-step pipelines with retries, conditional branching, and exactly-once semantics. |
| Ingestion and Indexing | Keep vector databases, knowledge graphs, and search indexes up-to-date as upstream sources change. |
| Massive Parallelization | Fan out to thousands of workers for batch processing and embarrassingly parallel workloads. |
| Mission-Critical Workloads | Workloads where retries, checkpointing, and replay are non-negotiable (payments, billing, compliance). |
| Event-Driven Architectures | Use events + CEL filters to route external signals into the right workflows without bespoke routing code. |

## Integrations

| Name | Description |
|------|-------------|
| PostgreSQL | The durability substrate; Hatchet ships with managed migrations and is happy on RDS, Cloud SQL, Neon, Supabase, or self-hosted Postgres. |
| RabbitMQ | Optional message bus for inter-service communication and high-throughput real-time updates. |
| Kubernetes | Official Helm chart at hatchet-dev/hatchet-charts for production self-hosting. |
| Docker | Hatchet Lite single-image deployment plus a production Docker Compose stack. |
| AWS (ECS, SNS) | ECS-friendly worker deployment patterns and first-class SNS alerting. |
| Slack | Native Slack alerting integration for run failures and SLA breaches. |
| GitHub | GitHub OAuth login for the dashboard plus repo-linked workflow source. |
| OpenTelemetry | Engine and SDKs emit OTel traces; the API exposes trace lookup. |
| Terraform | Official Terraform provider for managing Hatchet Cloud resources as code. |
| Homebrew | brew install via the hatchet-dev/homebrew-hatchet tap. |
| FastAPI | Documented quickstart for combining Hatchet Python SDK with FastAPI services. |
| Next.js | Multiple Next.js starter templates wire Hatchet into App Router and Pages Router projects. |
| Anthropic | Hatchet's durable-execution model is a natural substrate for orchestrating Anthropic Claude tool calls and multi-step agents; the hatchet-typescript-deep-research and hatchet-typescript-code-agent reference patterns illustrate the integration shape. |

## Solutions

| Name | Description |
|------|-------------|
| Hatchet Cloud | Fully managed orchestration engine on Hatchet's infrastructure with tier-included task-run allowances and SOC 2 / HIPAA controls. |
| Self-Hosted (Open Source) | MIT-licensed engine, API, dashboard, and Helm chart for running Hatchet on the operator's own infrastructure. |
| Hatchet Lite | Single-image bundled deployment of engine, API, and dashboard for development, testing, and low-throughput production. |
| Bring-Your-Own-Cloud (Enterprise) | Enterprise tier deploys the Hatchet engine inside the customer's own VPC while remaining managed by Hatchet. |

## Artifacts

Machine-readable API specifications organized by format.

### OpenAPI

- [Hatchet API (bundled OpenAPI 3.1)](openapi/hatchet-openapi.yml) — 141 operations across 23 resource tags

### JSON Schema

- [V1 Task](json-schema/hatchet-v1-task-schema.json)
- [V1 Workflow Run](json-schema/hatchet-v1-workflow-run-schema.json)
- [V1 Event](json-schema/hatchet-v1-event-schema.json)
- [V1 Filter](json-schema/hatchet-v1-filter-schema.json)
- [V1 Webhook](json-schema/hatchet-v1-webhook-schema.json)
- [V1 Task Event](json-schema/hatchet-v1-task-event-schema.json)
- [V1 Log Line](json-schema/hatchet-v1-log-line-schema.json)
- [Tenant](json-schema/hatchet-tenant-schema.json)
- [Worker](json-schema/hatchet-worker-schema.json)
- [Rate Limit](json-schema/hatchet-rate-limit-schema.json)
- [API Token](json-schema/hatchet-api-token-schema.json)
- [Workflow](json-schema/hatchet-workflow-schema.json)

### JSON Structure

- [V1 Task](json-structure/hatchet-v1-task-structure.json)
- [V1 Workflow Run](json-structure/hatchet-v1-workflow-run-structure.json)
- [V1 Event](json-structure/hatchet-v1-event-structure.json)
- [V1 Filter](json-structure/hatchet-v1-filter-structure.json)
- [V1 Webhook](json-structure/hatchet-v1-webhook-structure.json)
- [V1 Task Event](json-structure/hatchet-v1-task-event-structure.json)
- [V1 Log Line](json-structure/hatchet-v1-log-line-structure.json)
- [Tenant](json-structure/hatchet-tenant-structure.json)
- [Worker](json-structure/hatchet-worker-structure.json)
- [Rate Limit](json-structure/hatchet-rate-limit-structure.json)
- [API Token](json-structure/hatchet-api-token-structure.json)
- [Workflow](json-structure/hatchet-workflow-structure.json)

### JSON-LD

- [Hatchet Context](json-ld/hatchet-context.jsonld) — Linked-data context aligning Hatchet entities with schema.org

### Examples

- [Get Task](examples/v1-task-get-example.json)
- [Trigger Workflow Run](examples/v1-workflow-run-trigger-example.json)
- [Publish Event](examples/v1-event-create-example.json)
- [Create Filter](examples/v1-filter-create-example.json)
- [Cancel Tasks](examples/v1-task-cancel-example.json)
- [Replay Tasks](examples/v1-task-replay-example.json)
- [List Task Logs](examples/v1-log-line-list-example.json)
- [Upsert Rate Limit](examples/rate-limit-upsert-example.json)
- [Register Webhook Worker](examples/webhook-worker-create-example.json)
- [List Workers](examples/worker-list-example.json)

### Plans, Rate Limits, FinOps

- [Plans and Pricing](plans/hatchet-plans-pricing.yml) — Developer, Team, Scale, Enterprise, Self-Hosted
- [Rate Limits](rate-limits/hatchet-rate-limits.yml) — Per-tier throughput and engine-level rate-limit primitive
- [FinOps Mapping](finops/hatchet-finops.yml) — FOCUS-aligned, task-run as the primary billable unit

## Capabilities

Naftiko capabilities organized as shared per-API definitions composed into customer-facing workflows.

### Shared Per-API Definitions

- [Hatchet Orchestration](capabilities/shared/hatchet-orchestration.yaml) — 9 operations for triggering, observing, and controlling task and workflow runs
- [Events and Filters](capabilities/shared/hatchet-events-and-filters.yaml) — 8 operations for publishing events and binding them to workflows via CEL filters
- [Tenant Governance](capabilities/shared/hatchet-tenant-governance.yaml) — 11 operations for managing tenants, tokens, workers, and engine rate limits

## Vocabulary

- [Hatchet Vocabulary](vocabulary/hatchet-vocabulary.yml) — Controlled vocabulary covering 33 terms across 7 domains (Orchestration, Workflow, Execution, Event Ingestion, Observability, Governance, Deployment)

## Rules

- [Hatchet Ruleset](rules/hatchet-rules.yml) — 13 Spectral rules enforcing Hatchet's OpenAPI conventions (path namespacing, operation ID format, tag taxonomy, bearer auth, error schema standardization)

## Maintainers

**FN:** Kin Lane

**Email:** kin@apievangelist.com
