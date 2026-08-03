# Database Bible

## System of record

PostgreSQL is the canonical transactional store.

## Core tables

- `projects`
- `project_settings`
- `provider_credentials`
- `keywords`
- `keyword_metrics`
- `serp_snapshots`
- `serp_results`
- `competitors`
- `opportunities`
- `topic_clusters`
- `content_pages`
- `content_versions`
- `content_sources`
- `content_claims`
- `qa_runs`
- `qa_results`
- `workflow_runs`
- `workflow_tasks`
- `ai_executions`
- `model_usage`
- `publishing_targets`
- `publishing_jobs`
- `analytics_events`
- `ranking_snapshots`
- `conversion_events`

## Standards

- UUIDv7 primary keys
- UTC timestamps
- Explicit foreign keys
- `NOT NULL` by default
- JSONB only for genuinely flexible metadata
- Forward-only migrations
- Soft deletion only where recovery has user value

## Personal-edition simplification

No organization hierarchy is required. Data belongs directly to the operator and is separated by `project_id` where appropriate.

## Performance

Use composite indexes around `project_id`, status, and timestamps. Partition high-volume event and ranking tables only after measured need. Preserve raw provider snapshots in object storage when payload volume makes PostgreSQL inefficient.

## Backup

Automated encrypted backups, point-in-time recovery where supported, and periodic restore testing are required before the system is trusted with production work.
