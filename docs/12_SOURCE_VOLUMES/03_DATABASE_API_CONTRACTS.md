# Database, API and Contracts

Documents merged: **453**

This volume consolidates prior database conventions, table drafts, DDL fragments, migration notes, API groups, OpenAPI conventions, JSON schemas, events, and service-contract templates.

## Database direction

- PostgreSQL is the transactional source of truth.
- Use UUIDv7 identifiers, UTC timestamps, explicit status constraints, optimistic version columns, and soft deletion only where recovery or auditability requires it.
- Project-owned records carry `project_id`; provider credentials are encrypted and never placed in logs or events.
- Large event, ranking, and AI execution histories should be partitioned by time.
- Indexes must correspond to real access patterns; avoid speculative indexing.
- Schema changes use forward migrations and expand/migrate/contract deployment sequencing.

## Initial domains

- users and local identities;
- projects and project settings;
- keywords, metrics, clusters, opportunities, competitors, and SERP snapshots;
- content pages, briefs, versions, sources, claims, QA runs, and publications;
- AI tasks, workflow runs, prompt versions, agent runs, model usage, and cost records;
- analytics imports, ranking snapshots, conversions, and refresh recommendations.

## API direction

- OpenAPI 3.1 contract first.
- Base prefix: `/api/v1`.
- Plural resource names and cursor pagination.
- Stable machine-readable error codes.
- Idempotency keys for workflow creation, publication, imports, and other repeatable side effects.
- Long-running work returns `202 Accepted` and a workflow/task resource that can be streamed or polled.
- Every operation declares authentication, validation, error responses, examples, and observability requirements.

## Event direction

Event names follow `<context>.<entity>.<action>.v<major>`. Consumers assume at-least-once delivery and must be idempotent. Large payloads are stored in object storage and referenced by URI rather than embedded in events.
