# Infrastructure and Operations

Documents merged: **69**

This volume consolidates Docker, Kubernetes, Terraform, worker-cluster, observability, backup, disaster-recovery, deployment, release, queue, and operational-runbook drafts.

## Personal-edition deployment

Begin with Docker Compose or a small single-node deployment. The minimum stack is the web/API application, background worker, PostgreSQL, Redis, Qdrant, and S3-compatible object storage. Add ClickHouse, OpenSearch, NATS/Kafka, and Kubernetes only when workload or reliability evidence justifies them.

## Worker runtime

Tasks use leases, heartbeats, priorities, idempotency keys, exponential backoff with jitter, maximum-attempt policies, cancellation, and dead-letter handling. Scaling decisions use queue age, task cost, provider rate limits, CPU/memory, and concurrency safety.

## Observability

Capture structured logs, OpenTelemetry traces, application metrics, queue metrics, provider latency, token usage, AI cost, workflow success rate, publication outcomes, and SEO business metrics. Every incident must be traceable by request, workflow, task, and project identifiers.

## Reliability

Backups require point-in-time recovery for PostgreSQL, object-storage versioning, encrypted snapshots, restore drills, and documented RPO/RTO targets. Releases use health probes, migrations designed for compatibility, smoke tests, and rollback procedures.

## Cost discipline

Track infrastructure and AI cost by project and workflow. Prefer simpler infrastructure, managed services only where their operational value exceeds cost, and autoscaling limits that prevent runaway provider or worker spend.
