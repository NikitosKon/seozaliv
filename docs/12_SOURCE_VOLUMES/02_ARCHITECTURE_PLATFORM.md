# Architecture and Platform

Documents merged: **28**

This volume consolidates the earlier system architecture, DDD, service, event, workflow, repository, and platform-contract drafts.

## Canonical direction

- Start as a modular monolith with clearly separated bounded contexts.
- Split services only when independent scaling, failure isolation, or ownership makes the boundary valuable.
- Use synchronous APIs for direct queries and commands; use events for long-running workflows and cross-domain propagation.
- Keep PostgreSQL as the transactional source of truth, Redis for cache and leases, object storage for large artifacts, Qdrant for semantic memory, and ClickHouse only when analytics volume justifies it.
- Use an outbox pattern for reliable event publication.
- Every workflow is versioned, idempotent, observable, cancellable, and resumable.

## Core bounded contexts

- Projects and configuration
- SEO Intelligence
- Content Factory
- AI Runtime
- Quality Assurance
- Publishing
- Analytics and Optimization
- Provider Integrations

## Deployment model

The initial deployment may run as a small set of containers: web UI, API/platform process, AI worker, crawler/research worker, PostgreSQL, Redis, Qdrant, and object storage. Kubernetes remains an optional scaling target rather than an MVP requirement.

## Repository boundaries

`apps/` contains user-facing applications, `services/` domain modules, `workers/` asynchronous processors, `packages/` shared technical libraries, `docs/` canonical specifications, and `infrastructure/` deployment definitions. Business logic must not be hidden in generic shared packages.
