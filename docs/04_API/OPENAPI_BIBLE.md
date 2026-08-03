# OpenAPI Bible

## Scope

The personal edition exposes a versioned REST API for the web interface, workers, integrations, and future CLI tooling.

## Conventions

- Base path: `/api/v1`
- JSON request and response bodies
- Consistent error envelope
- Cursor pagination for large collections
- Idempotency keys for workflow creation and publishing commands
- Correlation IDs on every request and task

## Initial resources

- `/projects`
- `/keywords`
- `/serp-snapshots`
- `/competitors`
- `/opportunities`
- `/clusters`
- `/content-pages`
- `/content-versions`
- `/qa-runs`
- `/workflows`
- `/ai-executions`
- `/publishing-targets`
- `/publishing-jobs`
- `/analytics`
- `/settings/providers`

## Error shape

```json
{
  "status": "error",
  "code": "VALIDATION_ERROR",
  "message": "Request validation failed",
  "details": [],
  "request_id": "..."
}
```

## Async operations

Long-running work returns `202 Accepted` with a workflow or task identifier. Clients obtain progress through polling or server-sent events.

## Governance

The OpenAPI document is the contract. Breaking changes require a new API version or an explicit compatibility plan.
